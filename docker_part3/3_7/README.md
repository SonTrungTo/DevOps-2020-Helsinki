## This exercise will optimize the frontend and backend example of the course to its fullest potential
using techniques have been taught in the course.

## Frontend
- Pre-optimization: `652 MB` (see [3.1](https://github.com/SonTrungTo/DevOps-2020-Helsinki/tree/master/docker_part3/3_1))
- Post-optimization:

## Backend
- Pre-optimization: `443 MB` (see [3.1](https://github.com/SonTrungTo/DevOps-2020-Helsinki/tree/master/docker_part3/3_1))
- Post-optimization:

### Post-optimization uses these techniques:
- Multi-stage builds.
- Alpine version in appropriate builds.
- Non-root user.
- Trimming down unnecessary packages after builds.