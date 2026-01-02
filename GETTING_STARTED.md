# Getting Started

Never written a line of code? Perfect. This guide assumes nothing and gets you from zero to watching Claude automatically cancel your subscriptions in about 10 minutes.

## What You're About to Do

1. **Download this project** from GitHub (2 min)
2. **Install Claude Code** - a tool that lets an AI work on your computer (3 min)
3. **Export your transactions** from your bank as a spreadsheet (2 min)
4. **Run the audit** - Claude analyzes your spending and asks what to cancel (3 min)
5. **Watch the magic** - Claude opens Chrome and cancels subscriptions for you

No coding required. You'll type a few commands, but I'll show you exactly what to type.

---

## Step 1: Download This Project

You're on GitHub right now. GitHub is just a website where people share projects. Let's get this one onto your computer.

1. Look for the green **"Code"** button near the top of this page
2. Click it → Click **"Download ZIP"**
3. Find the downloaded file (probably in your Downloads folder)
4. Double-click to unzip it
5. You now have a folder called `just-fucking-cancel-main` - drag it somewhere easy to find (like your Desktop)

✅ **You now have the project on your computer.**

---

## Step 2: Install Claude Code

Claude Code is a tool that lets Claude (the AI) work directly with files on your computer and control your browser.

### What You'll Need
- **A Claude Pro subscription** ($20/month) - [Get it here](https://claude.ai/settings/billing)
- About 5 minutes for installation

### Mac Installation

1. **Open Terminal**
   - Press `Cmd + Space` (opens Spotlight search)
   - Type `Terminal`
   - Press Enter
   - A window with a black or white background and blinking cursor appears. This is Terminal.

2. **Install Claude Code**
   
   Copy this entire line and paste it into Terminal, then press Enter:
   ```
   curl -fsSL https://claude.ai/install-cli | sh
   ```
   
   Wait for it to finish (you'll see text scrolling, then it stops).

3. **Restart Terminal**
   - Close the Terminal window
   - Open Terminal again (same way as before)

### Windows Installation

1. **Open PowerShell**
   - Press the Windows key
   - Type `PowerShell`
   - Click "Windows PowerShell"

2. **Install Claude Code**
   
   Copy this entire line and paste it into PowerShell, then press Enter:
   ```
   irm https://claude.ai/install-cli.ps1 | iex
   ```
   
   Wait for it to finish.

3. **Restart PowerShell**
   - Close the window
   - Open PowerShell again

### Verify It Worked

In your Terminal/PowerShell, type:
```
claude --version
```

If you see a version number, you're good! If you see "command not found," restart your computer and try again.

✅ **Claude Code is installed.**

---

## Step 3: Export Your Bank Transactions

You need a CSV file (a type of spreadsheet) with your recent transactions.

### Apple Card
1. Open the **Wallet** app on your iPhone
2. Tap your **Apple Card**
3. Scroll down and tap **Card Balance**
4. Tap the **...** menu → **Export Transactions**
5. Choose **Last 12 Months** and **CSV**
6. Send it to yourself (AirDrop, email, etc.) and save to your computer

### Chase
1. Log in at chase.com
2. Click your account
3. Look for **Download account activity** (usually a download icon)
4. Select date range (last 12 months ideal)
5. Choose **CSV** format
6. Save the file

### Other Banks
Look for "Export," "Download," or "Download transactions" in your account. Choose CSV format (not PDF or Excel).

**Save your CSV file(s) into the `just-fucking-cancel-main` folder** you downloaded earlier.

✅ **You have your transaction data ready.**

---

## Step 4: Run the Subscription Audit

Now the fun part. You're going to navigate to your project folder and start Claude.

### Mac

1. **Open Terminal** (Cmd + Space → "Terminal" → Enter)

2. **Navigate to your project folder**
   
   If you put the folder on your Desktop, type this and press Enter:
   ```
   cd ~/Desktop/just-fucking-cancel-main
   ```
   
   (If you put it somewhere else, type `cd ` then drag the folder into Terminal - it will paste the path)

3. **Start Claude Code**
   ```
   claude
   ```
   
   The first time, it will ask you to log in. Follow the prompts.

### Windows

1. **Open PowerShell**

2. **Navigate to your project folder**
   
   If you put the folder on your Desktop, type:
   ```
   cd $HOME\Desktop\just-fucking-cancel-main
   ```

3. **Start Claude Code**
   ```
   claude
   ```

### Tell Claude What to Do

Once Claude is running, you'll see a prompt where you can type. Say:

```
Audit my subscriptions. I have transaction CSVs in this folder.
```

**What happens next:**
- Claude reads your transaction files
- Claude identifies recurring charges (Netflix, Spotify, gym memberships, etc.)
- Claude asks you questions: "Do you use Hulu?" "When did you last use Adobe?"
- You answer honestly
- Claude generates a beautiful HTML report showing what to cancel

**To see your report:** Claude will create an HTML file. Double-click it to open in your browser.

✅ **You've audited your subscriptions.**

---

## Step 5: Let Claude Cancel For You (The Magic Part)

This is where it gets wild. Claude can actually open Chrome and cancel subscriptions for you.

### Enable Browser Control

1. In the same Claude session, type:
   ```
   /permissions
   ```

2. Enable **Browser** permissions when prompted

3. Then tell Claude:
   ```
   Help me cancel the subscriptions I marked for cancellation. Open Chrome and walk me through each one.
   ```

### What You'll See

- Claude opens Chrome automatically
- Navigates to Netflix.com (or wherever)
- Clicks through the cancellation flow
- Asks for your confirmation before final steps
- Moves to the next subscription

You can watch, intervene, or let it run. You're always in control.

---

## Privacy & Security

**Your transaction data stays on your computer.** 

- Your CSV files never leave your machine
- Claude processes everything locally
- The generated audit report is a local HTML file
- Nothing is uploaded to any server

The only data that goes to Anthropic (Claude's company) is your conversation with Claude - not your raw transaction data.

---

## Troubleshooting

### "claude: command not found"
- Make sure you restarted Terminal/PowerShell after installing
- Try restarting your computer
- Run the installation command again

### "Permission denied" (Mac)
- Go to System Preferences → Privacy & Security
- Look for Claude Code and allow it

### Claude can't find my CSV
- Make sure the CSV file is in the `just-fucking-cancel-main` folder
- Make sure it's actually a `.csv` file (not `.xlsx` or `.pdf`)

### Browser control isn't working
- Make sure Chrome is installed (not Safari, Firefox, etc.)
- Try closing all Chrome windows first
- Grant permissions when Claude asks

### "I need to log in" when Claude opens a site
- That's normal! Log in yourself, then tell Claude to continue
- Claude can't (and shouldn't) know your passwords

---

## Cost

- **Claude Pro subscription**: $20/month ([sign up](https://claude.ai))
- **This project**: Free

You can cancel Claude Pro anytime after you've cleaned up your subscriptions. One month is usually enough.

---

## Questions?

- Open an issue on this GitHub repo
- Check the [Claude Code docs](https://docs.anthropic.com/en/docs/claude-code)

---

*Time to stop paying for things you don't use.*
