# Security – How I Implemented and Understood It

When I reached the security phase of my Quarkus journey, I realized it wasn’t just about “locking things up” — it was about trust, control, and responsibility.
I wasn’t only building APIs; I was creating systems that handle sensitive data, user access, and organizational logic. So, I decided to understand how security works end-to-end before writing a single line of code.

## Understanding the Essence of Security

Before I began implementing JWTs or roles, I asked myself:
“What exactly am I trying to protect?”

That question helped me shape my thinking.
I learned that security in backend systems has two key parts:

- Authentication — verifying who the user is.

- Authorization — defining what that user can do.

I realized that a good system doesn’t just let people in — it lets the right people in and keeps everything else locked down.

## Securing Endpoints with Roles

Once I understood the theory, I began applying it.
In my project, different users — like Admins, Sales Managers, and Regional Officers — needed different access levels.

That’s where I used role-based security.
Quarkus made this simple through the @RolesAllowed annotation.

Here’s an example of how I protected endpoints:

@Path("/sales")
@RolesAllowed({"Admin", "SalesManager"})
public class SalesResource {

    @GET
    @Path("/data")
    public Response getSalesData() {
        return Response.ok("Protected sales data").build();
    }

}

This taught me something powerful:
Security isn’t only about restricting access — it’s about structuring trust in your system.

### Learning and Using @RolesAllowed

When I first saw @RolesAllowed, I thought it was just another annotation — until I realized how much control it gives.
It ties directly into the user’s JWT token, checking what roles are embedded inside before allowing any request through.

So, if a token doesn’t include the required role, the endpoint automatically blocks the request — no extra logic needed.
That simplicity made my code cleaner, safer, and more professional.

## JWT Authentication – The Core of My Security Setup

JWT (JSON Web Token) became the heart of my authentication process.
I learned that instead of storing sessions, Quarkus issues a digitally signed token after login — proof that a user is who they claim to be.

Each token contains:

- The user’s username

- Their roles

- Optional identifiers like tenant_id and region_id

In my project, I used a service to generate JWTs like this:

var builder = Jwt.issuer("my-app")
.upn(username)
.groups(roles)
.claim("tenant_id", tenantId)
.claim("region_id", regionId);

return builder.sign();

At first, I didn’t realize how much was happening behind the scenes.
When that token got signed using my private key, it meant that only my backend could verify it — and no one could forge it.
That’s when I understood the power of cryptographic trust in modern apps.

## Exploring Quarkus OIDC and Keycloak

While building my custom JWT setup, I also explored how OIDC (OpenID Connect) works with Quarkus.
I discovered that OIDC extends OAuth2, making it possible to integrate professional tools like Keycloak for single sign-on (SSO) and centralized user management.

Even though I haven’t fully integrated Keycloak yet, learning about it opened my eyes to how enterprise systems manage users securely across multiple apps.
I now understand realms, clients, and tokens in a much deeper way — and I know it’s the next step as my system grows.

## Understanding OAuth2 – The Bigger Picture

OAuth2 helped me understand that security isn’t just about users — it’s also about how systems talk to each other.
It enables one service to access another without sharing passwords — using tokens instead.

I realized this is how companies like Google and Microsoft let apps safely connect to their APIs.
It made me think long-term: my system could one day support third-party integrations through the same secure standard.

## Securing REST Clients

Finally, I learned that security doesn’t end at the backend.
When one Quarkus service talks to another, the JWT token can be propagated, ensuring all internal requests are equally secure.

@RegisterRestClient(configKey = "sales-api")
public interface SalesRestClient {
@GET
@Path("/summary")
@RolesAllowed("Admin")
String getSummary();
}

This taught me consistency — the same token that verifies a user in one service can be trusted by another, keeping the security chain unbroken.

## What Security Taught Me

Security changed the way I see backend development.
I stopped thinking about “just coding features” and started thinking about building trust and reliability.
When users log in, I’m not just authenticating them — I’m protecting data, transactions, and the reputation of the system itself.

More importantly, I learned that we’re not just coding for fun —
we’re building systems that must be efficient, safe, and easy to debug even when they grow complex.

## Summary of My Security Journey

Concept showing What I Learned Applied in Project
Authentication & Authorization The difference and relationship between verifying identity and enforcing permissions ✅
Role-Based Access How to use @RolesAllowed to control endpoint access ✅
JWT Authentication How tokens are created, signed, and verified ✅
OIDC & Keycloak How enterprise identity management works 🔜
OAuth2 How secure delegated access is achieved 🔜
Securing REST Clients How to propagate security across microservices ✅
