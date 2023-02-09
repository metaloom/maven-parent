# MetaLoom Maven Parent

This is the central parent maven project for all MetaLoom projects.


## Release Process

```bash
# Update maven version to next release + Update jreleaser.yml version
mvn versions:set -DgenerateBackupPoms=false

# Check build
mvn clean package

# Deploy to maven central and auto-close staging repo. 
# Adding the property will trigger the profiles in the parent pom to include gpg,javadoc...
mvn clean deploy -Drelease
```