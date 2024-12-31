# Platform solution

...

## Grouping and selecting tasks
Before beginning any tasks I evaluated the complaints based on their complexity (based on my skillset and time limit) and their topography in dev ops terms. This led me to prioritise the complaints as follows.
#### Simple, code collaboration tooling
Using [pre-commit](https://pre-commit.com/) to manage git hooks. This solves code and proto formatting

#### Simple, local setup documentation
Record all CLI dependencies link to their respective platform-specific download/install pages

#### Less simple, use docker-compose for the local dev environment
Compose simplifies network and moves us towards docker-first development

#### Less simple, integrate Go Releaser with GHA to publish docker images for prod deployment
Best in class tooling for go builds.

#### Moderate, introduce an sql migration tool
By managing tables as SQL scripts with [golang-migrate](https://github.com/golang-migrate/migrate) we ensure that dev and prod use the same schemas. It also means that developers can share feature/schema changes via `git cherry-pick` or feature branches.

#### Challenging, deploying the app to a production environment via GHA
As there is currently no deployment or CI boilerplate, it would take a big jump to get an automated deployment up and running. To keep things simple, I'll try my hand at getting a [nomad](https://developer.hashicorp.com/nomad/tutorials/get-started/gs-overview) deployment setup.
