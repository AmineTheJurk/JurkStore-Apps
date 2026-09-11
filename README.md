# JurkStore-Apps

Official application repository for **JurkStore** on **JurkOS**.

This repository contains community and official software packages installable through the `JurkStore` TUI application in JurkOS.

---

## App Folder Structure

Every application in the store lives in its own folder inside `apps/`:

```text
JurkStore-Apps/
└── apps/
    └── [your-app-name]/
        ├── meta.xml          # Package descriptor (details below)
        └── [YourApp].bk      # The compiled Linux executable binary
```

---

## Understanding `meta.xml`

The `meta.xml` file tells JurkStore everything it needs to know about your application. It must be placed directly inside your app's directory.

### Example `meta.xml`

```xml
<?xml version="1.0" encoding="UTF-8"?>
<jurkos-app>
    <name>MyTool</name>
    <version>1.0.0</version>
    <author>YourName</author>
    <description>A fast and lightweight utility for JurkOS.</description>
    <download>https://raw.githubusercontent.com/AmineTheJurk/JurkStore-Apps/main/apps/mytool/MyTool.bk</download>
</jurkos-app>
```

### Tag Explanations

| Tag | Required | Description |
| :--- | :--- | :--- |
| `<name>` | **Yes** | The official display name of your app (e.g. `MyTool`). When installed, JurkStore also creates a shortcut in `/bin/[name]` so users can launch it by typing this name in the terminal. |
| `<version>` | **Yes** | The current version of your application (e.g. `1.0.0`). |
| `<author>` | **Yes** | Your name, username, or organization name (e.g. `AmineTheJurk`). |
| `<description>` | **Yes** | A clear, concise summary of what your application does. This is displayed in the JurkStore terminal interface when users inspect your app. |
| `<download>` | **Yes** | The direct raw URL where JurkStore can download your executable binary. Usually points to the raw GitHub link of your `.bk` file. |

> **Note:** JurkStore is a terminal application store, so **no icon tag is needed**. Keep your `meta.xml` strictly to the tags above.

---

## How to Submit Your App

Anyone can submit applications to the JurkStore! Follow these simple steps:

### 1. Fork the Repository
Click the **Fork** button at the top right of this repository ([github.com/AmineTheJurk/JurkStore-Apps](https://github.com/AmineTheJurk/JurkStore-Apps)) to create your personal copy under your GitHub account.

### 2. Add Your Files to Your Fork
In your forked repository, create a new folder under `apps/` with your app's name (for example, `apps/mytool/`):
- Add your **`meta.xml`** using the format explained above.
- Add your compiled binary file named with the **`.bk`** extension (for example, `MyTool.bk`).

### 3. Open a Pull Request (PR)
Once you have committed and pushed your new app files to your fork:
1. Go back to the main [JurkStore-Apps](https://github.com/AmineTheJurk/JurkStore-Apps) repository.
2. Click on the **Pull requests** tab and press **New pull request**.
3. Select your fork and branch, and click **Create pull request**.

### 4. Wait Patiently for Administrator Review
After creating your Pull Request:
- Please wait patiently while an administrator reviews your submission.
- An administrator will review your `meta.xml` and binary to ensure it works correctly and safely on JurkOS.
- Once accepted, an administrator will **merge** your Pull Request, successfully uploading your app to the official store!

