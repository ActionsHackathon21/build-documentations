Build documentations
===
*This project follows the DEV.to [#ActionsHackathon21](https://dev.to/devteam/join-us-for-the-2021-github-actions-hackathon-on-dev-4hn4) hackathon.*

Use GitHub Actions and Workflows to build your documentations with MkDocs, then publish to Github Pages.

![Screenshot](https://github.com/ActionsHackathon21/build-documentations/raw/main/screenshot.png)

![Result](https://github.com/ActionsHackathon21/build-documentations/raw/main/screenshot2.png)

Check the complete workflow here ([build-documentations.yml](.github/workflows/build-documentations.yml))

## Actions used
- **[actions/checkout@v2](https://github.com/actions/checkout)** To checkout the source code from the repository
- **[actions/cache@v2](https://github.com/actions/cache)** To cache the dependencies, allow us to re use them for future builds


## Configurations
- You can config the branch which holds the documentations with `DOCUMENTATIONS_BRANCH` variable. 
- You can also configure the branches which you want to run this workflow, with `branches` key.
- To configure the Github pages, you can go to **settings** > **pages** > **Source** and choose the documentation branch.


![Config](https://github.com/ActionsHackathon21/build-documentations/raw/main/screenshot2.png)


## Flows
- Use **[actions/checkout@v2](https://github.com/actions/checkout)** to checkout source code from the repository
- Use **[actions/cache@v2](https://github.com/actions/cache)** to cache dependencies (`.pip` directory)
- Install dependencies with `pip`
- Build documentations with Mkdocs
- Synchronize built files with deployment branch
- Push build into the deployment branch
