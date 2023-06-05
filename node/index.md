## Status

| Release        | Status     | Initial    | Active LTS | LTS Version | Maint LTS  | End Of Life |
| :------------- | :--------- | :--------- | :--------- | :---------: | :--------- | :---------- |
| [8](./v8.md)   | EOL        | 2017-05-30 | 2017-10-31 |             | 2019-01-01 | 2019-12-31  |
| [10](./v10.md) | EOL        | 2018-04-24 | 2018-10-30 |   10.13.0   | 2020-05-19 | 2021-04-30  |
| [12](./v12.md) | EOL        | 2019-04-23 | 2019-10-21 |   12.13.0   | 2020-10-20 | 2022-04-30  |
| [14](./v14.md) | Maint LTS  | 2020-04-21 | 2020-10-27 |   14.15.0   | 2021-10-19 | 2023-04-30  |
| [16](./v16.md) | Maint LTS  | 2021-04-20 | 2021-10-26 |   16.13.0   | 2022-10-18 | 2023-09-11  |
| [17](./v17.md) | EOL        | 2021-10-19 |            |             | 2022-04-01 | 2022-06-01  |
| [18](./v18.md) | Active LTS | 2022-04-19 | 2022-10-24 |   18.12.0   | 2023-10-22 | 2025-04-30  |
| [19](./v19.md) | Maint      | 2022-10-18 |            |             | 2023-04-01 | 2023-06-01  |
| [20](./v20.md) | Current    | 2023-04-18 | 2023-10-24 |             | 2024-10-22 | 2026-04-30  |

[Release change logs](https://github.com/nodejs/node/tree/main/doc/changelogs), [History](https://github.com/nodejs/node/commits/main/doc/changelogs)

<br><hr>

## v8

### version

`node -p "process.versions['v8']"`


### harmony flags

- `node --v8-options | grep "in progress" | sort`
- `node --v8-options | grep -v "in progress" | grep harmony | sort`


## upgrading npm

There is no handy way to update node package manager (npm) via the node version manager for windows. Below are the steps to perform the upgrade manually.

1. `nvm use <version to upgrade>`
1. `cd $NVM_HOME/version to upgrade`
1. `mv npm.cmd npm1.cmd`
1. Delete all remaining npm-related files, `rm -f npm npx.cmd npx npm.ps1 npx.ps1`.
1. `npm1 install -g npm`
