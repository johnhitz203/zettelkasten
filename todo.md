# Todo

## Research
- [ ] Dynamic Dispatching
- [ ] Duck Typing

You can create todos in Foam.

- [x] This is an example of a todo list item that's complete
- [ ] This one is not completed yet
- [ ] You can mark it completed by pressing `Option`+`C` (or `Alt`+`C`) when your cursor is on this line
  - [ ] You can also select multiple lines and mark them all at once!

config :mindery, Mindery.Mailer,
    adapter: Swoosh.Adapters.Sendgrid,
    api_key: env!("SendGrid_API_KEY")
  #  api_key: System.get_env("SendGrid_API_KEY")

  config :swoosh,
    api_client: Swoosh.ApiClient.Finch,
    finch_name: Mindery.Finch
end
