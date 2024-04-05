# fly.io

## SSH Into App

- Setup There is a one-time step that is required to communicate with the app over ssh[1]
  ```
  $ Fly ssh issue --agent
  ```

- Open a Console - Use the following command with the app-name to open a remote terminal[1]
  ```
  $ fly cosnole --pty -C "/app/bin/<app-name> remote"
  ```

- Create a Shell Scrip - Create a file named riex (short for remote iex) with the following contents. Make it executable with the chmod command, and run it with ./fiex.[1]
  ```
  #/bin/bash

  set -e

  fly ssh console --pty -select -C "/app/bin/<app-name> remote"
  ```
  ```
  $ chmod +x riex
  ```
    <pre>The --select flag prompts for which instance to connect to. This is useful when running different instance in different regions.</pre> 

## Launch





1. https://fly.io/docs/elixir/the-basics/iex-into-running-app/

[[index]]