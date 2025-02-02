---
outline: deep
head:
  - - meta
    - property: og:title
      content: CapsuleSigner • signMessage
  - - meta
    - name: description
      content: Overview of the signMessage method on CapsuleSigner
  - - meta
    - property: og:description
      content: Overview of the signMessage method on CapsuleSigner
---

# signMessage

`signMessage` supports signing messages from the `CapsuleSigner`.

This method must be called after [`authenticate`](/packages/aa-signers/capsule/authenticate). Otherwise, this method will throw an error with the message `Not Authenticated`.

## Usage

::: code-group

```ts [example.ts]
import { createCapsuleSigner } from "./capsule";
// [!code focus:99]
const capsuleSigner = await createCapsuleSigner();

const signedMessage = await capsuleSigner.signMessage("test");
```

<<< @/snippets/capsule.ts
:::

## Returns

### `Promise<Hex>`

A Promise containing the signature of the message.

## Parameters

### `msg: string | Uint8Array)` -- the message to sign
