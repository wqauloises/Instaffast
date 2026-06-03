# InstafFast - Instagram Widget App

A lightweight, simple Android widget to display Instagram follower and following counts directly on your home screen.

## ✨ Features

- ✅ **Instagram Only** - Focused exclusively on Instagram profiles
- ✅ **Simple Design** - Clean, minimal dark theme interface
- ✅ **Dual Metrics** - Display both followers AND following counts
- ✅ **Easy Setup** - Just enter your Instagram username
- ✅ **Manual Refresh** - Tap the refresh button to update counts
- ✅ **Profile Link** - Tap profile picture to open Instagram
- ✅ **Auto-restart** - Widget survives device reboot
- ✅ **Dark Mode** - Beautiful dark theme UI

## 📱 Installation

### Option 1: Download APK
1. Go to [Releases](../../releases) section
2. Download the latest `instaffast-release.apk`
3. Open the APK file on your Android device
4. Allow installation from unknown sources if prompted
5. App installed! ✅

### Option 2: Build from Source
1. Clone this repository:
```bash
git clone https://github.com/wqauloises/instaffast.git
cd instaffast
```

2. Open in Android Studio (2023.1+)
3. Click "Build" → "Build Bundle(s) / APK(s)" → "Build APK(s)"
4. Wait for the build to complete
5. APK will be in `app/build/outputs/apk/release/`

## 🎯 How to Use

### Adding the Widget
1. Long-press on your Android home screen
2. Select "Widgets"
3. Search for "InstafFast"
4. Select and drag to place on home screen
5. A configuration screen will appear

### Configuring
1. Enter your Instagram username (with or without @)
2. Or paste your Instagram profile URL
3. Tap "Save Widget"
4. Widget will fetch and display your stats!

### Refreshing
- Tap the refresh button (↻) on the widget to update counts
- Widget auto-updates every 30 minutes

## 📊 What's Displayed

On the widget, you'll see:
- **@username** - Your Instagram handle
- **Followers count** - Total followers
- **Following count** - Total accounts you follow
- **Profile Picture** - Your latest profile photo
- **Refresh Button** - Manual refresh control

## ⚙️ Requirements

- **Android**: 7.0 (API 24) or higher
- **Internet**: Active connection required for fetching data
- **Instagram**: Public profile (private profiles may not work)

## 🏗️ Project Structure

```
instaffast/
├── app/
│   ├── src/main/
│   │   ├── java/com/instaffast/
│   │   │   ├── MainActivity.java
│   │   │   ├── MyApplication.java
│   │   │   ├── InstafWidget.java
│   │   │   ├── WidgetConfigureActivity.java
│   │   │   ├── InstagramService.java
│   │   │   └── WidgetConfigManager.java
│   │   └── res/
│   │       ├── layout/
│   │       ├── drawable/
│   │       ├── values/
│   │       └── xml/
│   └── build.gradle.kts
├── gradle/
├── build.gradle.kts
├── settings.gradle.kts
└── README.md
```

## 🔧 Core Components

| File | Purpose |
|------|---------|
| `InstafWidget.java` | Main widget provider & UI updater |
| `WidgetConfigureActivity.java` | Widget configuration screen |
| `InstagramService.java` | Scrapes Instagram profile data |
| `WidgetConfigManager.java` | Persistent widget storage |
| `BootReceiver.java` | Restores widgets after reboot |

## 🎨 Customization

### Change Colors
Edit `app/src/main/res/values/colors.xml`:
```xml
<color name="instagram_pink">#E1306C</color>
<color name="dark_bg">#121212</color>
```

### Modify Update Frequency
Edit `app/src/main/res/xml/widget_info.xml`:
```xml
android:updatePeriodMillis="1800000" <!-- 30 minutes -->
```

## 🐛 Troubleshooting

### Widget shows "---" for counts
- Check your internet connection
- Verify username is correct
- Ensure Instagram profile is public

### Widget not updating
- Tap the refresh button
- Remove and re-add the widget
- Restart your device

### "Not configured" message
- Tap the widget
- Enter your Instagram username
- Tap "Save Widget"

## 📝 License

This project is open source and available under MIT License.

## ⚠️ Disclaimer

- This app is not affiliated with Instagram or Meta
- Data fetching is done by scraping public Instagram pages
- Use responsibly and respect Instagram's terms of service
- Instagram may change their website structure, breaking this app

## 🚀 What's New (v1.0)

✨ Initial Release
- Instagram-only widget (no Spotify/YouTube)
- Followers + Following counts
- Simple, clean dark UI
- Manual refresh button
- Profile tap to Instagram
- Widget persistence after reboot

## 💡 Future Features

- [ ] Multiple widget instances
- [ ] Engagement metrics (likes, comments)
- [ ] Post count display
- [ ] Widget themes/color picker
- [ ] Followers/Following comparison
- [ ] Growth notifications

## 📧 Support

Have issues? Open an [Issue](../../issues) on GitHub!

---

**Made with ❤️ for Instagram fans**

Download the APK from [Releases](../../releases) and start using InstafFast today! 🚀
