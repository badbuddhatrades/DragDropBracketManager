# Drag-Drop Bracket Manager for NinjaTrader 8

**Simplify your bracket order placement with an intuitive drag-and-drop interface**

A NinjaTrader 8 addon that streamlines bracket order management by letting you visually set your stop loss and take profit levels directly on the chart with a simple drag motion. Available in both **LITE** (free) and **PRO** (paid) versions.

---

## What is Drag-Drop Bracket Manager?

Drag-Drop Bracket Manager transforms how you place bracket orders in NinjaTrader 8. Instead of manually calculating risk/reward ratios and entering prices, simply drag on your chart to set one level, and the tool automatically calculates the other based on your chosen risk/reward ratio.

### Perfect For
- Day traders who need quick bracket order placement
- Traders who want consistent risk management
- Anyone looking to reduce order entry errors
- Scalpers and position traders alike

---

## How It Works

1. **Enter a position** (Long or Short) in NinjaTrader
2. **Enable the tool** by clicking the button or using a hotkey (PRO)
3. **Drag on the chart** to set your level:
   - **Drag DOWN** to set your Stop Loss (Take Profit auto-calculates)
   - **Drag UP** to set your Take Profit (Stop Loss auto-calculates)
4. **Release** - Orders submit immediately with your chosen risk/reward ratio
5. Tool auto-disables for safety

### Example: Long Position at ES 4500 (1:2 R:R)

**Option 1 - Set Stop Loss by dragging down:**
- Drag to 4490 (10 points risk)
- Tool calculates TP at 4520 (20 points reward)
- Result: 1:2 ratio ✓

**Option 2 - Set Take Profit by dragging up:**
- Drag to 4520 (20 points reward)
- Tool calculates SL at 4490 (10 points risk)
- Result: 1:2 ratio ✓

Both methods give the same result - choose whichever feels more natural!

---

## Version Comparison

### LITE Version (Free)

**Best for:** Beginners and traders who want simple, consistent risk management

**Core Features:**
- Fixed 1:2 Risk:Reward ratio (the most popular professional ratio)
- Drag direction logic Long: (down for SL, up for TP), Short: (up for SL, down for TP)
- Visual yellow preview line while dragging
- Simple one-button toggle
- Auto-disable after placing orders for safety
- User-based license (works on unlimited machines)
- Weekly automatic update checking

**What's NOT included:**
- No configurable R:R ratios (locked to 1:2)
- No hotkey support
- No real-time price overlay
- No position scaling (multiple bracket sets)
- No sound alerts
- No settings window
- No debug logging

### PRO Version (Paid)

**Best for:** Active traders who need customization and advanced features

**Everything in LITE, plus:**

**Advanced Risk Management:**
- 6 Risk:Reward ratio presets: 1:1, 1:2, 1:3, 2:1, 3:1, Custom
- Cycle through ratios instantly with hotkey
- Custom ratio configuration for unique strategies

**Enhanced User Experience:**
- Real-time visual overlay showing R:R, Entry, SL, TP during drag
- Hotkey support: Toggle tool (Ctrl+Shift+B), Cycle R:R (Ctrl+Shift+R)
- Sound alerts for success, errors, and R:R changes
- Arrow indicators showing which value you're setting vs. calculated

**Professional Features:**
- Multiple bracket sets for position scaling
  - Example: Exit 50% @ 1:1, 30% @ 1:2, 20% @ 1:3
  - Each set uses its own R:R ratio
  - Perfect for scaling out of winning positions
- Comprehensive settings window with 5 configuration tabs
- Debug logging to file for troubleshooting
- Daily automatic update checking
- Customizable overlay positioning (TopRight, TopLeft, FollowMouse)

**Hotkey Shortcuts:**
- `Ctrl+Shift+B` - Toggle bracket tool on/off
- `Ctrl+Shift+R` - Cycle through R:R presets

---

## Feature Comparison Table

| Feature | LITE (Free) | PRO (Paid) |
|---------|-------------|------------|
| **Risk:Reward Ratios** | Fixed 1:2 only | 1:1, 1:2, 1:3, 2:1, 3:1, Custom |
| **Drag Direction Logic** | ✅ Yes | ✅ Yes |
| **Visual Preview Line** | ✅ Yes (yellow line) | ✅ Yes (yellow line) |
| **Real-time Price Overlay** | ❌ No | ✅ Yes (shows exact prices) |
| **Toggle Button** | ✅ Yes | ✅ Yes (+ settings gear) |
| **Hotkey Support** | ❌ No | ✅ Toggle + Cycle R:R |
| **Position Scaling** | ❌ No | ✅ Multiple bracket sets |
| **Sound Alerts** | ❌ No | ✅ Yes (configurable) |
| **Settings Window** | ❌ No | ✅ Yes (5 tabs) |
| **Debug Logging** | ❌ No | ✅ Yes (to file) |
| **Auto-disable After Order** | ✅ Yes | ✅ Yes |
| **User-Based License** | ✅ Yes | ✅ Yes |
| **Update Checking** | ✅ Weekly | ✅ Daily |
| **Multi-Machine Support** | ✅ Unlimited | ✅ Unlimited |
| **Best For** | Beginners, testing | Active traders, professionals |

---

## Installation

### LITE Version

1. Download the LITE `.zip` file
2. Open NinjaTrader 8
3. Go to **Control Center → Tools → Import → NinjaScript Add-On**
4. Select the LITE `.zip` file
5. Click **Import**
6. Press **F5** to compile
7. Restart NinjaTrader


### PRO Version

1. Purchase PRO license from BadBuddha Customs LLC
2. Download the PRO `.zip` file
3. If you have LITE installed: **Tools → Remove NinjaScript Assembly → Select LITE → Remove**
4. Follow steps 2-7 from LITE installation above
5. License activates automatically (user-based)

**Note:** Do not install LITE and PRO simultaneously to avoid conflicts.

---

## Quick Start Guide

### Basic Usage (Both Versions)

1. **Open a chart** with Chart Trader enabled (Ctrl+T)
2. **Enter a position** (Long or Short)
3. **Click the button** to enable:
   - LITE: "Bracket LITE: OFF" → turns green "Bracket LITE: ON"
   - PRO: "Bracket PRO: OFF (1:2)" → turns green "Bracket PRO: ON (1:2)"
4. **Drag on the chart**:
   - **Long**: Drag DOWN for SL or UP for TP
   - **Short**: Drag UP for SL or DOWN for TP
5. **Release** - Orders submit immediately
6. Tool auto-disables

### PRO-Only Features

**Change Risk:Reward Ratio:**
- Press `Ctrl+Shift+R` to cycle through presets
- Or open settings window (gear icon) to set custom ratio

**Quick Toggle:**
- Press `Ctrl+Shift+B` to enable/disable without clicking button

**Position Scaling:**
- Enable "Use Bracket Sets" in settings
- Configure percentages and R:R ratios for each set
- Example: 50% @ 1:1, 30% @ 1:2, 20% @ 1:3

---

## System Requirements

- **NinjaTrader:** Version 8.1.6.0 or higher
- **Operating System:** Windows
- **License:** User-based license (works on unlimited machines tied to your NinjaTrader account)
- **Active NinjaTrader License:** Required

---

## Support & Documentation

### Getting Help
- **Email:** support@badbuddhatrades.com
- **Website:** https://badbuddhatrades.com
- **GitHub:** https://github.com/badbuddhatrades/BadBuddhaCustoms

### Reporting Issues
When reporting bugs, please include:
1. NinjaTrader version
2. Addon version (LITE or PRO)
3. Steps to reproduce
4. Screenshots if possible

---

## Frequently Asked Questions

**Q: Is LITE really free?**
A: LITE requires a user-based license but is free to use. The license allows unlimited installations on machines tied to your NinjaTrader account.

**Q: Can I use this with live trading?**
A: Yes, with a valid license. **Always test in simulation first!** The addon executes real orders immediately when you release your drag.

**Q: Why only 1:2 ratio in LITE?**
A: 1:2 is the most popular and balanced risk/reward ratio used by professional traders. It keeps the LITE version simple while covering 80% of use cases. For flexibility, upgrade to PRO.

**Q: Can I upgrade from LITE to PRO?**
A: Yes! Purchase PRO, uninstall LITE via Tools → Remove NinjaScript Assembly, then import PRO. Your user-based license transfers automatically.

**Q: Does it work with Sim and Live accounts?**
A: Yes, both versions work with Sim and Live accounts.

**Q: How does position scaling work in PRO?**
A: You configure multiple "bracket sets" with different percentages and R:R ratios. For example: 50% of position exits @ 1:1, 30% @ 1:2, 20% @ 1:3. Each set creates separate OCO bracket orders.

**Q: Can I customize the hotkeys in PRO?**
A: Yes, hotkeys are fully customizable in the PRO settings window.

**Q: Will LITE receive updates?**
A: Yes, LITE receives bug fixes and compatibility updates. Major new features go to PRO first.

---

## Risk Warning & Disclaimer

**Trading involves substantial risk of loss.** This addon is a tool to help execute your trading decisions - YOU are responsible for those decisions.

- Always test in simulation before using with real money
- Understand how bracket orders work before using this tool
- The tool places orders immediately when you release your drag
- No warranty is provided - use at your own risk
- Past performance does not guarantee future results

---

## License & Terms

### Usage Rights

Licensed users may:
- ✅ Use on unlimited computers (tied to NT account)
- ✅ Use with Sim and Live accounts
- ✅ Receive updates and support

You may NOT:
- ❌ Reverse-engineer or modify the compiled code
- ❌ Sell or redistribute
- ❌ Share your license with others

### Warranty

**NO WARRANTY PROVIDED.** This software is provided "as is" without warranty of any kind. Use at your own risk.

---

## About BadBuddha Customs LLC

We build practical trading tools for real traders. Our philosophy:
- **Simple workflows** that don't slow you down
- **Reliable code** that works when you need it
- **Fair pricing** with free options available
- **Responsive support** when you have questions

### Other Tools
Visit https://badbuddhatrades.com to explore our other NinjaTrader addons and trading tools.

---

## Get Started Today

### Try LITE (Free)
Perfect for testing the drag-and-drop workflow and getting comfortable with bracket orders.
- Simple 1:2 R:R ratio
- No configuration needed
- Risk-free way to try the tool

### Upgrade to PRO
Ready for more control? PRO gives you:
- Full R:R customization
- Hotkeys for faster trading
- Position scaling capabilities
- Professional-grade features

**Download Lite:** [https://github.com/badbuddhatrades/DragDropBracketManager](https://github.com/badbuddhatrades/DragDropBracketManager/raw/refs/heads/main/DragDropBracketAddOnLite.zip)

**Download Pro:** [https://github.com/badbuddhacustoms/DragDropBracketManager](https://github.com/badbuddhatrades/DragDropBracketManager/raw/refs/heads/main/DragDropBracketAddonProv2.3.zip)

**Purchase PRO:** https://badbuddhatrades.com

---

**Thank you for using Drag-Drop Bracket Manager!**

*© 2025 BadBuddha Customs LLC | User-Based Licensing Available*
