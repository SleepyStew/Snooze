# Snooze branding refactor notes

During the Mail-0/Zero -> Snooze rebrand sweep, the following follow-up issues were identified:

1. **Legacy technical identifiers remain**
   - Database table prefixes (`mail0_*`), migration filenames, backend class names (e.g. `ZeroAgent`) and other internal identifiers are deeply coupled to existing deployments.
   - Renaming these safely requires coordinated migrations and backend/client compatibility work.

2. **Pricing code still exists but is no longer surfaced**
   - Public route and primary UI entry points to pricing were removed.
   - Pricing components (`apps/mail/components/pricing/*`, `apps/mail/components/ui/pricing-dialog.tsx`) remain in the codebase as technical debt and can be removed in a dedicated cleanup PR.

3. **Localized translation coverage is incomplete for full rebrand consistency**
   - Not all language packs were rewritten in this pass to avoid breaking translation keys.
   - Some non-English copy may still include historical naming terms.

4. **External links/contact endpoints are placeholders**
   - Social/contact links were updated away from Mail-0/Zero references where practical, but should be validated against your canonical Snooze accounts/domains before public release.

