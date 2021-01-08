# Newton Evolution Proposals (NEPs)

[![Join the chat at https://gitter.im/newtonproject/NEPs](https://badges.gitter.im/newtonproject/NEPs.svg)](https://gitter.im/newtonproject/NEPs?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Newton Evolution Proposals (NEPs) describe Proposals for the Newton Project including *Economic Model*, *Personnel*, *Technical*, *Community Governance* and *Business*.

We welcome anyone with suggestions related to Newton Project to compile a NEP.  

This repository tracks the ongoing status of NEPs. It contains:

- `Draft` LINK-TO-BE-ADDED proposals which intend to complete the NEP review process.
- `Public Call` LINK-TO-BE-ADDED for proposals that may become `Final` / `Active` (see also RSS feed).
- The NEP process that governs the NEP repository.

Browse all current and draft NEPs on the official NEPs site. LINK-TO-BE-ADDED

Newton Evolution Proposals (NEPs) repository exists as a place to share concrete proposals with potential users of the proposal and the Newton community at large.

## NEP Guidelines

Docs for Guides are located in `./NEPs/guides/` directory.

Visit website for live.

## Local Development

### Prerequisites

1. Open Terminal.

2. Check whether you have NodeJS and Yarn installed:

```bash
node --version && yarn --version
```

If you don't have NodeJS or Yarn installed, install them from [NodeJS Download](https://nodejs.org/en/download/) and [Yarn Installation](https://yarnpkg.com/getting-started/install).

3. Clone repository and update git submodules

```bash
git clone --recursive git@github.com:newtonproject/NEPs.git
```

Then go into your cloned git directory

```bash
cd NEPs
```

4. Install Dependencies:

```bash
yarn
```

### Start Website in Dev Mode

```bash
yarn dev
```

### Build Website Files

```bash
yarn build
```
