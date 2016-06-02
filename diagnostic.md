# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    A pokedex is made up of pokemon components, which individually have components for different stats, types, and moves, which could be expanded when the pokemon is clicked upon.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    A new tempate file is made under the app/components dir, in which HTMLbars for that component is put - this tells any views that use this component what to show.
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{#each model as |contact|}}
      {{#my-contact title=contact.title}}
        {{contact.body}}
      {{/my-contact}}
    {{/each}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{#each contact.body as |body|}}
      {{my-contact/my-phone body=body}}
    {{/each}}
    ```
