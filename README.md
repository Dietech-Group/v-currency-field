# Vuetify Currency Field
The Vuetify Currency Field uses [Vue Currency Input](https://dm4t2.github.io/vue-currency-input/) directive to create a currency component (`<v-currency-field>`) with all features of v-text-field.
The component is compatible with vuetify 1.x and 2.x and dynamic binds the props and listeners to v-text-field component.

`Lightweight`
Only [~4 kB bundle size](https://bundlephobia.com/result?p=v-currency-field) (minified + gzipped).

[Read the guide](https://phiny1.github.io/v-currency-field/) to getting started.


### Dietech Branch

- The project was forked and all customizations have been done in the `dietech` branch.
- When a new version of the original package is released do the following:

  - Sync new changes of main branch via github ui
  - Pull changes and rebase customized branch. You may need to resolve merge conflicts while rebasing.

    ```
    git checkout main
    git pull
    git checkout dietech
    git rebase main
    git push
    ```

  - Trigger the github action to release a new version ([release.yml](.github/workflows/release.yml)) with creating a new tag (starting with `v`) and push it:

    ```
    git tag <tagname>
    git push origin <tagname>
    ```

    The naming scheme of the tags should be: `v<package-version>-dietech.<change-version>`. The `<package-version>` is the current version of the forked repo. The `<change-version>` is the number of the release of the current customized package version. It restarts wit `0` for every new `<package-version>`.
    <br><br>
    Example: `v3.1.1-dietech.0` (1st release of the customized package version 3.1.1)
