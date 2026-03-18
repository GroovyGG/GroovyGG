# Fix WakaTime: "API not provided" and stats not showing

## 1. Fix WakaTime inside Cursor (so your coding time is tracked)

If Cursor says the WakaTime API key is not provided:

1. **Get your API key**
   - Go to [https://wakatime.com/settings/account](https://wakatime.com/settings/account)
   - Sign in (or create an account)
   - Copy your **API Key**

2. **Install the WakaTime extension in Cursor**
   - Open Extensions: `Cmd+Shift+X` (Mac) or `Ctrl+Shift+X` (Windows/Linux)
   - Search for **WakaTime**
   - Install **WakaTime** by WakaTime

3. **Give Cursor your API key**
   - After installing, Cursor may prompt you to enter your API key; paste it there.
   - Or set it manually:
     - Open Settings: `Cmd+,` (Mac) or `Ctrl+,` (Windows/Linux)
     - Search for **wakatime**
     - Find **WakaTime: Api Key** and paste your key

4. **Use Cursor for a bit**
   - Code for a few minutes so WakaTime can send data. After a while, check [https://wakatime.com/dashboard](https://wakatime.com/dashboard) to see if time appears.

---

## 2. Fix WakaTime in your GitHub Profile README (the stats block)

The "Weekly Coding Breakdown" section is filled by a **GitHub Action**. The workflow is now at the **repo root**: `GroovyGG/.github/workflows/waka-readme.yml` (so GitHub will run it).

1. **Add secrets in this repo (GroovyGG)**
   - Open **https://github.com/GroovyGG/GroovyGG** → **Settings** → **Secrets and variables** → **Actions**
   - Click **New repository secret** and add:
     - **Name:** `WAKATIME_API_KEY`  
       **Value:** your WakaTime API key (same as in Cursor)
     - **Name:** `GH_TOKEN`  
       **Value:** a [GitHub Personal Access Token](https://github.com/settings/tokens) with `repo` and `user` scope

2. **Run the workflow once**
   - In this repo, go to **Actions** → **Waka Readme** → **Run workflow**
   - When it finishes, it will update the root README and replace the `<!--START_SECTION:waka-->` block with your WakaTime stats.

If the API key wasn’t set in GitHub Secrets before, the action could not fetch WakaTime data; after adding the secrets and re-running the workflow, the stats should appear.
