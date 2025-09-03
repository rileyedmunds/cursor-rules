# Code Review Checklist

Review the changes on @branch:

## Data Flow & Architecture
- Think through how data flows in the app. Explain new patterns if they exist and why.
- Were there any changes that could affect infrastructure?

## User Experience States
- Consider empty, loading, error, and offline states.

## Frontend Quality
- Review frontend changes for a11y (keyboard navigation, focus management, ARIA roles, color contrast).

## API & Compatibility
- If public APIs have changed, ensure backwards compatibility (or increment API version).

## Dependencies & Performance
- Did we add any unnecessary dependencies? If there's a heavy dependency, could we inline a more minimal version?
- Are there places we should use caching?

## Testing Strategy
- Did we add quality tests? Prefer fewer, high quality tests. Prefer integration tests for user flows.

## Database & Schema
- Were there schema changes which could require a database migration?

## Security & Auth
- Changes to auth flows or permissions? Run /security-review.

## Feature Management
- If feature flags are set up, does this change require adding a new one?

## Internationalization
- If i18n is set up, are the strings added localized and new routes internationalized?

## Observability
- Are we missing critical o11y or logging on backend changes?
