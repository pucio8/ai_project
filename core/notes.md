# YAML

- **System Prompt** (prompts) -> system prompt (kcal).md
- **Models** (providers) -> google:gemini-3-flash-preview
- **Tests** ->
  1. icontains - czy w odpowiedzi modelu znajduje się dany ciąg znaków, ignorując wielkość liter.
  2. javascript - Pozwala na uruchomienie kodu JS, który analizuje odpowiedź (output).
  3. not-icontains - Test przechodzi tylko wtedy, gdy w odpowiedzi nie ma podanego słowa.

## Składnia

**Klucze i listy** (spacje są krtycznie ważne)
**Klucze**: Zapisywane jako klucz: wartość.
**Listy**: Zaczynają się od myślnika -.

Tests to root key : wartością jest lista

- vars x3 to trzy oddzielne testy

prompts:

- system prompt (kcal).md

providers:

- id: geminai

tests:
#Test 1

- vars:  
   user_input : "Message"
  assert: - type: ....
  value: ...
  #Test 2..
- vars:  
   user_input : "Message"
  assert:
  - type: ....
    value: ...
