# part0_excercise4
```mermaid
graph LR;
First_Action;

Form-->Input --> Save --> Browser_sends_User_Input_to_the_server;
```
Submitting the Form Causes 5 HTTP requests.

```mermaid
graph TD;
sequenceDiagram
  participant Submit
  participant Reload
  participant main.css
  participant main.js
  participant data.json

  Submit ->> Reload: sends POST request to address new_note server response 302
  Reload ->>Fetch: causes 3 more HTTP requests
  Fetch ->> main.css
  Fetch ->> main.js
  Fetch ->> data.json
```
