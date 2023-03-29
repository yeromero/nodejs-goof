# Deploying the Goof app to Heroku

## Step-by-step tutorial

1. Sign-up to a free plan at heroku (<https://www.heroku.com>)
2. Install the `heroku` CLI. If you're on a macOS:

    ```bash
    brew install heroku/brew/heroku
    ```

3. Authenticate to Heroku and follow the instructions with the following command:

    ```bash
    heroku login
    ```

4. Change directories to the goof/ app repository you cloned/forked
5. Create a heroku app:

    ```bash
    heroku create
    ```
  
6. You'll have to update a Credit Card number at <https://heroku.com/verify> in order to enable the MongoDB addon next.

7. Add the MongoDB addon:

    ```bash
    heroku addons:create mongolab:sandbox
    ```

8. Push the Goof app to be deployed on the heroku platform

    ```bash
    git push heroku master
    ```

## Trouble-shooting

- If you need to inspect the logs

```bash
heroku logs --tail
```

- If you need to manually restart the deployed app:

```bash
heroku ps:scale web=1
```
