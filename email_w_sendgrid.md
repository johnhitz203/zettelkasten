# email_w_sendgrid

## Create a SendGrid API_KEY
1. Login to SendGrid
2. Navigate to settings > API Keys 
3. Click Create API Key in upper left corner
4. Copy to safe location
  Note: key is only displayed at time of creation.

## Create A .envrc File
```
export SENDGRID_API_KEY=<SENDGRID_API_KEY>
export SENDGRID_DOMAIN=<SENDGRID_DOMAIN>
export DATABASE_URL=ecto://postgres:postgres@localhost/whodapet_dev
export SECRET_KEY_BASE=<SECRET_KEY_BAS>
```

## Configure Application to use SendGrid

* In `config/runtime.exs` 
  ```
  if config_env() == :prod or config() == :dev do
    config :whodapet, Whodapet.Mailer,
        adapter: Swoosh.Adapters.Mailgun,
        api_key: System.get_env("MAILGUN_API_KEY"),
        domain: System.get_env("MAILGUN_DOMAIN")
  
    config :swoosh, :api_client, Swoosh.ApiClient.Finch
  end
  ```
* In `'lib/application_name/application.ex` include `{Finch, name: Swoosh.Finch}` in children


