# Shared bride-side Convex deployment

The root invitation and `wedding-only` site use the same Convex HTTP endpoint and the same schema in this folder. The bride-side production project is deployed in Europe (Ireland), so responses from the old groom-side database are not reused.

- Project: `xavier-sir-wedding-invitation-main`
- Production deployment: `colorful-perch-89`
- Attendance endpoint: `https://colorful-perch-89.convex.site/attendance`

From the repository root:

1. Authenticate with Convex if you need to redeploy this project.
2. Deploy the existing `convex/` functions and schema to the shared production deployment.
3. Keep the exact same attendance URL in both `site-config.js` and `wedding-only/site-config.js`.
4. Deploy the root folder to the main Netlify site and `wedding-only` as the second Netlify site.

The backend supports both variants through the `variant` request value: the full site accepts `betrothal` and `wedding`, while the wedding-only site is restricted to `wedding`.
