# vatsim-auth-node

You need to obtain VatsimAuth.dll to use this package, it is not provided here as "The VatsimAuth source code is proprietary, and VatsimAuth is not distributed under any license terms. All rights are reserved. Specifically, you may not distribute copies of VatsimAuth."

# Usage

- After you get your VatsimAuth.dll, place it right in the entry point of your project.

For example, this is the structure of a project using vatsim-auth-node package:

- example-project
  - node_modules
    - .bin
    - typescript
    - vatsim-auth-node
    - something else...
  - index.js
  - index.ts
  - package-lock.json
  - package.json
  - tsconfig.json
  - VatsimAuth.dll

- Include it in your project

```js
const VatsimAuth = require("vatsim-auth-node");
```

Or in typescript

```ts
import VatsimAuth from 'vatsim-auth-node';
// Check if the package has been loaded successfully
if(VatsimAuth.PackageVerify())
{
    console.log(VatsimAuth.ClientPublicKey());// Output: xxxxx(some number)
    console.log(VatsimAuth);
    // Output:
    // {
    //   GenerateAuthResponse: [Getter],
    //   GenerateAuthChallenge: [Getter],
    //   ClientPublicKey: [Getter],
    //   PackageVerify: [Getter],
    //   default: {
    //     GenerateAuthResponse: [Function (anonymous)],
    //     GenerateAuthChallenge: [Function (anonymous)],
    //     ClientPublicKey: [Function (anonymous)],
    //     PackageVerify: [Function (anonymous)]
    //   }
    // }
}
```

## Detailed usage is not provided.