# DFE-Digital-funding-service-cfs-fundingDataZone-schema


## Overview

The Funding Data Zone Schema repository contains the database schema definitions, scripts, and related assets used by the Funding Data Zone (FDZ).

The repository serves as the source of truth for schema management and supports the creation, evolution, and deployment of data structures used within the Calculate Funding Service (CFS) data platform.

## Purpose

This repository is responsible for:

- Managing Funding Data Zone database schemas.
- Version controlling schema changes.
- Supporting automated deployment pipelines.
- Providing a consistent and auditable approach to schema evolution.
- Enabling downstream reporting, analytics, and data migration processes.

## Repository Structure

```text
/
├── schema/
│   ├── tables/
│   ├── views/
│   ├── stored-procedures/
│   └── functions/
│
├── scripts/
│   ├── deployment/
│   ├── migration/
│   └── validation/
│
├── pipelines/
│
└── documentation/
```

## Prerequisites

Before working with this repository ensure you have:

- Git
- Access to the relevant Azure subscriptions
- SQL Server tooling (SSMS, Azure Data Studio, or equivalent)
- Required service permissions

## Deployment

Schema deployments are performed through the CI/CD pipeline.

Typical deployment flow:

1. Create a feature branch.
2. Implement schema changes.
3. Raise a Pull Request.
4. Obtain approval from code owners.
5. Merge into the target branch.
6. Automated deployment pipeline publishes the changes.

## Development Guidelines

### Naming Standards

- Use meaningful object names.
- Follow existing schema naming conventions.
- Avoid breaking changes where possible.
- Ensure scripts are idempotent when applicable.

### Schema Changes

For every schema modification:

- Include migration scripts.
- Validate against non-production environments.
- Consider backward compatibility.
- Document significant changes.

## Testing

Before submitting changes:

- Verify scripts execute successfully.
- Validate schema integrity.
- Check for impacts on existing pipelines.
- Confirm reporting and downstream dependencies are not affected.

## Branch Strategy

| Branch | Purpose |
|---------|----------|
| main | Production-ready code |
| develop | Active development |
| feature/* | New work |
| hotfix/* | Production fixes |

## Contributing

1. Create a feature branch.
2. Commit changes with meaningful commit messages.
3. Raise a Pull Request.
4. Complete peer review.
5. Merge after approval.

## Support

For questions or issues, contact the Funding Data Zone maintainers or raise an issue within this repository.

## Related Repositories

- Calculate Funding Service
- Funding Data Zone Pipelines
- Funding Data Zone Infrastructure
- Funding Data Zone Data Migration

## License

Unless otherwise stated, this repository is intended for internal use within the Department for Education.
