# TAP plugin test build

Download `tap.hpi` using GitHub's **Download raw file** button and upload it in Jenkins under **Manage Jenkins → Plugins → Advanced settings → Deploy Plugin**, then restart Jenkins.

This is a test build of the Commons Lang3 fix from source commit `33e5f53f448219570382204ef8a6b4748b2f0560`, based on the interim NPE fix in `baa4b0c4eaa07536f080142732ff6e4401026565`.

- Built with Java 17 and Maven 3.9.9 using `mvn -DskipTests package` after all 57 tests passed.
- Requires Commons Lang3 API plugin version `3.13.0-62.v7d18e55f51e2` or newer, plus the existing JUnit and Matrix Project dependencies. Install missing dependencies through Jenkins' plugin manager before deploying.
- Jenkins 2.582+ has not been directly tested; this build is intended for validation in that environment.
- SHA-256: `1137cd4b2ddbd50948f5e361fb9e086580258e6681f27a64b576e43516349426`.

Rebuild this artifact whenever the plugin source changes; it is not updated automatically.
