# Quickstart for Bitasmbl project (Ember.js)

## 1) Install Bitasmbl-CLI package

```bash
npm i bitasmbl-cli
```

## 2) Run bitasmbl command to set up the project

```bash
bitasmbl pull --repoUrl https://github.com/he1snber8/Bitasmbl_zaparojets_472_445 --appId 445 --repoId 302
```

## 3) Enter into the main directory and start coding!

```bash
cd Bitasmbl_zaparojets_472_445
```

## Customize requirements in a way you like

Bitasmbl organizes development into requirements. Each requirement describes a feature or implementation goal and can define suggested file locations through a `paths` array.

The `paths` property acts as a mapping guideline, helping contributors understand where related code should live.

You can customize `paths` mappings through the `bitasmbl.json` file.

{"Requirement":"Define portfolio layout","Paths":["**/src/layouts/**","**/src/components/layout/**","**/src/pages/**","**/src/routes/**","**/app/**"]}

## Requirement Evaluation

Bitasmbl includes a requirement evaluation workflow that lets contributors select a task and submit work for validation.

Run:

```bash
bitasmbl evaluate
```

Example output:

<pre>
? Available Requirements:

❯ [<span style="color:#9333ea">1</span>] <span style="color:#9333ea"> Define portfolio layout </span>            [3]
  [2] Build showcase components            [3]
  [3] Implement navigation routing         [3]
</pre>

`[x]` on the right represents the number of submission attempts remaining for a requirement.

## Example evaluation result

```js
/*
|--------------------------------------------------------------------------
| BITASMBL EVALUATION
|--------------------------------------------------------------------------
| REQUIREMENT:
| Implement project showcase UI
|
| SCORE: 21/100
| STATUS: FAIL ✕
|
| INSIGHT:
| The route renders static showcase data and does not use a component-driven
| structure, loading state, reusable card UI, or data abstraction.
|--------------------------------------------------------------------------
*/

import Route from "@ember/routing/route";

export default class ProjectsRoute extends Route {
  model() {
    return [
      {
        id: 1,
        title: "Portfolio Website",
        description: "Personal portfolio built with Ember.",
      },
      {
        id: 2,
        title: "Task Manager",
        description: "Simple productivity app.",
      },
    ];
  }
}
```

## Learn More

For complete command references, workflow explanations, and additional documentation, visit:

👉 [Bitasmbl Documentation](https://bitasmbl.com/docs)
