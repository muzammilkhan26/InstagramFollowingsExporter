# Instagram Followings Exporter

A powerful GUI application to export and track your Instagram followings list with detailed analytics and change tracking.

## 🌟 Features

- **Easy-to-use GUI** - Simple drag & drop interface
- **Cookie-based Authentication** - Secure login using browser cookies
- **Multiple Export Formats** - CSV, JSON, and Excel with formatting
- **Detailed User Information** - Fetch follower counts, bio, verification status
- **Change Tracking** - Monitor who you followed/unfollowed over time
- **Advanced Filtering** - Filter by verified accounts, private accounts
- **Profile Thumbnails** - Embed profile pictures in Excel exports
- **Batch Processing** - Handle large following lists efficiently

## 📋 Requirements

- Python 3.8 or higher
- Valid Instagram account
- Browser cookies.txt file

## 🚀 Installation

1. **Clone the repository:**
```
git clone https://github.com/muzammilkhan26/InstagramFollowingsExporter.git
cd InstagramFollowingsExporter
```

2. **Install dependencies:**
```
pip install -r requirements.txt
```

3. **Run the application:**
```
python main.py
```

## 🔧 Setup Instructions

### Step 1: Export Instagram Cookies

1. **Install a browser extension** to export cookies:
   - Chrome: "Get cookies.txt LOCALLY" or "cookies.txt"
   - Firefox: "cookies.txt" extension

2. **Export cookies:**
   - Go to Instagram.com and make sure you're logged in
   - Use the extension to export cookies as `cookies.txt`
   - Save the file to your computer

### Step 2: Use the Application

1. **Launch the app:** Run `python main.py`
2. **Load cookies:** Drag & drop your `cookies.txt` file or browse to select it
3. **Choose output folder:** Select where you want to save the exported data
4. **Configure options:**
   - ✅ **Fetch stats & bio** - Get detailed user information (slower)
   - ✅ **Verified only** - Export only verified accounts
   - ✅ **Private only** - Export only private accounts
   - ✅ **Embed thumbnails** - Add profile pictures to Excel file

5. **Click "Download Followings"** and wait for completion

## 📊 Output Files

The application generates several files:

- **`followings_username_YYYYMMDD_HHMMSS.csv`** - Basic CSV format
- **`followings_username_YYYYMMDD_HHMMSS.json`** - JSON format with all data
- **`followings_username_YYYYMMDD_HHMMSS.xlsx`** - Formatted Excel with hyperlinks
- **`added_YYYYMMDD_HHMMSS.csv`** - Newly followed accounts (if any)
- **`removed_YYYYMMDD_HHMMSS.csv`** - Unfollowed accounts (if any)

## 📈 Data Fields

Each export includes:

| Field | Description |
|-------|-------------|
| Username | Instagram username |
| Profile Link | Direct link to profile |
| Full Name | Display name |
| Verified | Verification status (YES/NO) |
| Private | Private account status (YES/NO) |
| User ID | Internal Instagram user ID |
| Profile Pic URL | Profile picture URL |
| Followers | Follower count (if detailed fetch enabled) |
| Followings | Following count (if detailed fetch enabled) |
| Bio | Profile biography (if detailed fetch enabled) |

## ⚠️ Important Notes

- **Rate Limiting:** The app includes built-in delays to avoid Instagram's rate limits
- **Cookie Expiry:** Cookies expire periodically - re-export them if you get authentication errors
- **Large Lists:** For accounts following 1000+ users, enable "Fetch stats & bio" only if needed (much slower)
- **Privacy:** This tool only accesses your own following list - it cannot access private data of other users

## 🛠️ Troubleshooting

### "Session invalid ya expired hai"
- Re-export cookies.txt from your browser
- Make sure you're logged into Instagram in the browser
- Clear browser cache and re-login if needed

### "Username se user_id parse nahi ho paya"
- Check if your account is still active
- Verify cookies.txt file is not corrupted
- Try logging out and back into Instagram

### Application won't start
- Ensure Python 3.8+ is installed
- Install all requirements: `pip install -r requirements.txt`
- Check if all dependencies installed correctly

## 🔒 Privacy & Security

- **Local Processing:** All data processing happens locally on your computer
- **No Data Sharing:** No information is sent to external servers
- **Cookie Safety:** Cookies are only used to authenticate with Instagram's API
- **Open Source:** Full source code available for review

## 📝 License

This project is for educational purposes only. Please respect Instagram's Terms of Service and use responsibly.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## ⭐ Support

If you find this tool helpful, please give it a star on GitHub!

---

**Disclaimer:** This tool is not affiliated with Instagram. Use at your own risk and in compliance with Instagram's Terms of Service.