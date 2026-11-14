# Israeli Family Budget

A single-page monthly budget calculator for parents in Israel, in shekels. English and Hebrew (RTL).

- Income, expenses and savings, with what is left each month
- About 110 built-in categories (Bituach Leumi allowances, arnona, va'ad bayit, tzaharon, keren hishtalmut, kupat gemel le-hashka'a, Savings for Every Child and more)
- Add or remove categories and groups, or create your own
- Amounts can be monthly, every two months or yearly
- Six ready-made templates, plus your own saved templates

## Use

Open `index.html` in a browser, or host it with GitHub Pages (Settings → Pages → deploy from the `main` branch, root folder). There is no build step and no server.

## Shared data in a GitHub JSON file

By default the budget is kept in the browser's local storage. To share it between devices and people:

1. On GitHub, create a fine-grained personal access token limited to the repository that should hold the data, with the **Contents** permission set to **Read and write**.
2. In the calculator, open **GitHub sync**, check the owner, repository, branch and file path (default `data/budget.json`), paste the token and press **Connect**.

The page then loads the budget from that file and commits every change back to it. Each person or device connects once with a token. The token is stored only in that browser and is never written to the file.

The JSON file is as visible as the repository it lives in. If this repository is public, point GitHub sync at a private repository instead, or make this one private.
