# Flower Power: New Version Package Attack Exercise

## Context Story

Recently, the shop started using a package repository to keep their software up to date. At first, the upload server was open to anyone, but the owner soon realized that this was not secure. To improve security, he added a password to the upload server. He also made other changes..

However, a new version of the `flower-power` package has appeared, and the shop's system is set to automatically update to the latest version.

Checkout what changed on the website..

The services are running on the same network named "workshop".

Look the hint only after you have tried to solve the exercise and one by one.

<details>
        <summary>Hint 1</summary>
        <p>
            As you can see a second source server has appeared but is offline, how about spinning up a local pypi server and uploading the malicious package to it to see if the app updates?
        </p>
</details>

<details>
        <summary>Hint 2</summary>
        <p>
            You should create a second instance of pypi server running behind pypi.local:8080 using docker. Create a Dockerfile that build an image for your local pypi server and run it in the same network as the exercise's services.
        </p>
</details>

## How to Run
0. **Don't read the source code!** Don't use a LLM for help!

1. Run

   ```sh
   DOCKER_BUILDKIT=0 docker compose build --no-cache
   docker compose up -d 
   ```
2. Open your browser and go to `http://localhost:5000`

If you need a rebuild(you are not supposed to need one)

   ```sh
   DOCKER_BUILDKIT=0 docker compose build --no-cache
   docker compose up -d
   ```

3. **Stop and clean up**

   ```sh
   docker compose down -v --remove-orphans
   ```

### Notes

- If you see "failed to find target default" during build, run the rebuild command above with `DOCKER_BUILDKIT=0`.

