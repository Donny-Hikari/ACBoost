
# WABoost

A simple tool that helps you WA faster, therefore AC faster.

## Usage

1. Create a new project

    ```shell
    . ./create <problem_name> [problem_url]
    ```

    This will create a new project under `$(date +%Y)/$problem_name` and cd into it.

2. Type your answer in `src/${problem_name}.cpp`.

3. Edit some cases and their answers in `cases/*.in`, `cases/*.out`.

4. Run test

    ```shell
    make test
    ```

    Or simply just `make`.

5. Enjoy your WAs and ACs.

## Advance Usage

1. Use custom theme.

    Custom theme can be load by specifing `ACBOOST_THEME` variable.

    ```shell
    ACBOOST_THEME=$ACBOOST_ROOT/ac_boost make test
    ```

    You can provide your own theme and use it this way. Refer to [themes/default](themes/default) to learn more.

2. You can put the variables in your shell login script to preserve your configuration.

    Edit `~/.bashrc` (if you use bash).

    ```shell
    ACBOOST_ROOT=$your_ACBOOST_ROOT
    ACBOOST_THEME=$ACBOOST_ROOT/themes/ac_boost
    ```
