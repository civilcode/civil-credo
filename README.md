# CivilCredo

CivilCode's in-house Credo rules.

## Installation

To your list of dependencies in `mix.exs`:

```elixir
def deps do
  [
    {:civil_credo, github: "civilcode/civil-credo", only: [:dev, :test], runtime: false},
  ]
end
```

and `.credo.exs`.

```elixir
%{
  configs: [
    %{
      name: "default",
      # 1. Configure the plugin
      plugins: [
        {CivilCredo, []}
      ]
    }
  ]
  checks: [
    # 2. Add this after existing checks
    # Custom checks from Plugin
    #
    {CivilCredo.Check.Design.TagWip, []},
    {CivilCredo.Check.Warning.UnsafeStruct, []}
  ]
}
```

## About the CivilCode Collective

The [CivilCode Collective](http://www.civilcode.io), a group of freelance developers, build tailored business applications 
in [Elixir](http://elixir-lang.org/) and [Phoenix](http://www.phoenixframework.org/)in Montreal, Canada.
