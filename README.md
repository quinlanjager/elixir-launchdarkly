# ExLaunchDarkly

A quick Elixir wrapper around the official LaunchDarkly [Erlang library](https://github.com/launchdarkly/erlang-server-sdk)

## Installation

```elixir
def deps do
  [
    {:ex_launch_darkly, github: "pixelunion/exlixir-launch-darkly", tag: "v0.0.1"}
  ]
end
```

## Usage

Start your connection to LaunchDarkly on Application start.

```elixir
ExLaunchDarkly.start(application.fetch_env!(:your_application, :launchdarkly_api_key)
```

Retrieve a variation.

```elixir
ExLaunchDarkly.variation("Some-Flag", ExLaunchDarkly.User.new("SomeUser"), false)
```