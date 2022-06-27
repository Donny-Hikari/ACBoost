
# ACBoost

A simple tool that helps you WA faster, therefore AC faster.

## Usage

1. Create a new project

    ```shell
    . acboost-create <problem_name> [problem_url]
    ```

    This will create a new project under `$(date +%Y)/$problem_name` and cd into it.

2. Type your answer in `src/${problem_name}.cpp`.

3. Edit some cases and their answers in `cases/*.in`, `cases/*.out`.

4. Run test

    ```shell
    make test
    ```

    Or simply just `make`.

    An example output (with the ac_boost theme).

    ![AC example](docs/ac-example.png)

5. Enjoy your WAs and ACs.

## Advance Usage

1. Use custom theme.

    Custom theme can be load by specifing `ACBOOST_THEME` variable.

    ```shell
    ACBOOST_THEME=$ACBOOST_ROOT/themes/ac_boost make test
    ```

    You can provide your own theme and use it this way. Refer to [themes/default](themes/default) to learn more.

2. You can put the variables in your shell login script to preserve your configuration.

    Edit `~/.bashrc` (if you use bash).

    ```shell
    ACBOOST_ROOT=$your_ACBOOST_ROOT
    ACBOOST_THEME=ac_boost # load theme from $ACBOOST_ROOT/themes/

    # use this to boost your access to ACBoost
    alias acboost-create=". $ACBOOST_ROOT/acboost-create"
    ```

3. Specify your own prefix when creating new project.

    By default projects will be created under `$(date +%Y)`. You can specify your own prefix.

    ```shell
    ACBOOST_DIRPREFIX=easy_problems acboost-create problem_a
    ```

    You can also specify this parameter via your login script.

4. Test ACBoost itself.

    ```shell
    cd metatest
    # Create test projects
    make create-test-projects
    # Run test
    make test
    ```

## FAQ

1. Cannot execute scripts.

    Grant permission to the scripts.

    ```shell
    chmod ug+x acboost-create
    chmod ug+x scripts/*
    ```
