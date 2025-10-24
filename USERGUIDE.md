# Drag-and-Drop Bracket Order Manager - User Guide

## What Is This Tool?

The Drag-and-Drop Bracket Manager is a **visual order entry tool** for NinjaTrader 8 that lets you set Stop Loss (SL) and Take Profit (TP) orders by simply clicking and dragging on your chart.

**Instead of typing numbers**, you drag to the price level you want, and the tool automatically places OCO (One Cancels Other) bracket orders.

## Key Benefits

✅ **Visual placement** - See exactly where your orders will be
✅ **Automatic mirroring** - Set one level, the other is calculated for you
✅ **Consistent risk/reward** - SL and TP are equidistant from your entry
✅ **Fast execution** - Place brackets in under 2 seconds
✅ **Works with Chart Trader** - No need to use strategies
✅ **Safety features** - Auto-disables after placing orders
✅ **Automatic updates** - Get notified when new versions are available

## Installation

### Step 1: Compile the AddOn

1. Open the NinjaTrader Control Center
2. Click **Tools → Import → NinjaScript Addon...**

3. Go to the location you downloaded the DragDropBracketManager.zip

4. Select the file and click Open.

6. **Restart NinjaTrader** (important!)

### Step 2: Verify Installation

1. Open any chart

2. Enable **Chart Trader** (right panel)

3. Look for a button in the **top-right corner** of Chart Trader that says:
   ```
   Bracket Tool: OFF
   ```

If you see the button, installation succeeded! 🎉

## How to Use

### Basic Workflow

1. **Enter a position** using Chart Trader (Long or Short)

2. **Enable the tool** by clicking the "Bracket Tool: OFF" button
   - Button turns **GREEN** and says "Bracket Tool: ON"

3. **Click and drag** on the chart:
   - **Drag DOWN** (below entry) to set your Stop Loss
   - **Drag UP** (above entry) to set your Take Profit

4. **Release the mouse** to place orders

5. **Tool auto-disables** (button turns red) to prevent duplicates

### Visual Guide

```
Price Chart:

4120 ← TP (automatically mirrored)
     |
     |
4100 ← Your Entry (Long position)
     |
     |
4080 ← You drag HERE (sets SL)

Result: SL at 4080, TP at 4120 (both 20 points from entry)
```

## Step-by-Step Example

### Example 1: Long Position

**Scenario:** You bought ES at 4500.00

1. Click "Bracket Tool: OFF" → turns GREEN
2. Click at 4480 and drag down
3. Yellow line appears showing 4480
4. Release mouse
5. **Orders placed:**
   - Stop Loss: 4480 (20 points below entry)
   - Take Profit: 4520 (20 points above entry, mirrored)

### Example 2: Short Position

**Scenario:** You sold NQ at 15000.00

1. Click "Bracket Tool: OFF" → turns GREEN
2. Click at 15050 and drag up
3. Yellow line appears showing 15050
4. Release mouse
5. **Orders placed:**
   - Stop Loss: 15050 (50 points above entry)
   - Take Profit: 14950 (50 points below entry, mirrored)

## Understanding the Mirroring Logic

The tool automatically calculates the opposite bracket level:

### For LONG Positions:

| You Drag To... | Sets... | Mirrors... |
|----------------|---------|------------|
| Below entry | Stop Loss | Take Profit above entry |
| Above entry | Take Profit | Stop Loss below entry |

### For SHORT Positions:

| You Drag To... | Sets... | Mirrors... |
|----------------|---------|------------|
| Above entry | Stop Loss | Take Profit below entry |
| Below entry | Take Profit | Stop Loss above entry |

**Example:**
- Long entry @ 100
- You drag to 95 (5 points below)
- **SL = 95** (what you dragged to)
- **TP = 105** (mirrored 5 points above)
- **Risk = Reward** (both 5 points)

## Visual Feedback

### Yellow Preview Line

While dragging, you'll see a **yellow dashed line** across the chart:
- Shows the exact price level where your mouse is
- Updates in real-time as you drag
- Disappears when you release the mouse

### Button States

| Button Text | Color | Meaning |
|-------------|-------|---------|
| "Bracket Tool: OFF" | Red | Tool disabled - clicks do nothing |
| "Bracket Tool: ON" | Green | Tool enabled - ready to drag |

After placing orders, the button automatically turns **OFF** (red) for safety.

## Tips & Best Practices

### ✅ DO:

- **Enable the tool only when ready to place orders**
- **Drag a reasonable distance** (at least a few pixels for accuracy)
- **Use on Sim account first** to get comfortable
- **Check your Chart Trader account is correct** before dragging
- **Wait for chart to fully load** before using (especially on startup)

### ❌ DON'T:

- **Don't leave the tool enabled** - turn it off when not in use
- **Don't click without dragging** - must move at least 2 pixels
- **Don't use without a position** - you need an existing position first
- **Don't use with strategy-managed positions** - use Chart Trader entries only

## Troubleshooting

### Problem: Button doesn't appear

**Solution:**
- Make sure Chart Trader panel is visible (right side of chart)
- Restart NinjaTrader

### Problem: Nothing happens when I click the chart

**Check:**
1. Is the button **GREEN** (ON)? If red, click it first.
2. Do you have an **active position**? Tool only works with existing positions.
3. Are you **dragging** (not just clicking)? Must drag at least 2 pixels.

**If still not working:**
- Open **Tools → Output Window** and look for error messages
- Make sure chart has fully loaded (all bars visible)

### Problem: Orders placed at wrong price

**This usually means the chart scale wasn't ready yet.**

**Solution:**
- Wait a few seconds after opening the chart before using the tool
- Try clicking on the chart to "wake up" the price scale
- Check that prices on the right axis look correct

### Problem: "Invalid SL" or "Invalid TP" message

**This means your drag created an invalid bracket:**

**For Long positions:**
- Stop Loss must be **below** your entry price
- Take Profit must be **above** your entry price

**For Short positions:**
- Stop Loss must be **above** your entry price
- Take Profit must be **below** your entry price

**Solution:** Try dragging in the opposite direction.

### Problem: Tool stays enabled (won't turn off)

**The tool auto-disables after placing orders.**

**If it doesn't:**
- Click the button manually to turn it OFF
- This shouldn't happen, but manual toggle always works

## Advanced Usage

### Working with Multiple Charts

- Each chart has its **own button** and **independent state**
- You can enable on one chart and disable on another
- Orders are always placed on the chart where you drag

### Using with Different Instruments

The tool works with **any instrument** (ES, NQ, CL, 6E, etc.):
- Price calculations adjust automatically
- Works with different tick sizes
- Works with forex, futures, and stocks

### Market Replay

The tool works perfectly with Market Replay:
- Can be used while replay is paused
- Can be used while replay is running
- Great for practicing entries on historical data

## Keyboard Shortcuts

Currently, there are **no keyboard shortcuts**. Everything is mouse-driven:
- Click button to enable/disable
- Click and drag to place orders

## Frequently Asked Questions

### Q: Can I adjust the SL/TP ratio?

**A:** Not currently. Both levels are always equidistant from entry (1:1 risk/reward). This is by design for consistent risk management.

### Q: What if I want asymmetric brackets (e.g., 1:2 risk/reward)?

**A:** You'll need to manually adjust one of the orders after placement, or use Chart Trader's native bracket tools.

### Q: Does this work with ATM strategies?

**A:** No, this tool places standalone OCO orders, not ATM-managed orders. It's designed for Chart Trader manual trading.

### Q: Can I use this for scaling in/out?

**A:** Not directly. The tool places brackets for your entire position. For scaling, you'd need to manually manage partial closes.

### Q: What happens if I drag while the tool is OFF?

**A:** Nothing. The tool only responds to mouse events when enabled (button is green).

### Q: Can I see the exact SL/TP prices before placing?

**A:** Not currently - you'll see the yellow preview line but not the calculated prices. Check your Orders tab after placement to see exact levels.

### Q: Are the orders GTC (Good Till Cancelled)?

**A:** Yes, all orders are placed as GTC (Good Till Cancelled). They won't expire at end of day.

### Q: What order types are used?

**A:**
- Stop Loss: **Stop Market** order
- Take Profit: **Limit** order

### Q: Can I use this for options or stocks?

**A:** The code is designed for NinjaTrader 8, which primarily supports futures and forex. Stocks may work but haven't been tested.

## Safety Features

The tool includes several safety mechanisms:

1. **Auto-disable after placing orders** - Prevents accidental duplicate brackets
2. **Requires active position** - Can't place orphan orders
3. **Validates SL/TP prices** - Rejects invalid bracket levels
4. **Requires meaningful drag** - Ignores tiny mouse movements (< 2 pixels)
5. **Toggle button** - Must explicitly enable before use

## Automatic Updates

This tool includes the **BadBuddha Update Service** which automatically checks for new versions.

### How It Works

- **Automatic check** - Once per day, the tool checks for updates in the background
- **No interruption** - Update checks happen silently, won't affect your trading
- **Notification popup** - If a new version is available, you'll see a popup with:
  - Current version vs. latest version
  - Release date and file size
  - Changelog (what's new)
  - Direct download link
- **Your choice** - Click "Open Download" to get the update, or "Remind Me Later" to dismiss

### What to Expect

When an update is available, you'll see a window titled:
```
BadBuddha Drag-Drop Bracket Manager — Update Available
```

The popup shows:
- Version comparison (e.g., Current: 1.0.0, Latest: 1.1.0)
- What's new in the update
- Any breaking changes (if applicable)
- Download button to get the latest version

### Privacy

- No personal data is collected
- Only checks version numbers from GitHub
- No tracking or analytics
- Completely optional - you can dismiss update notifications

## Getting Help

If you encounter issues:

1. **Check this guide first** - Most problems are covered above
2. **Check NinjaTrader Output Window** - Tools → Output Window
3. **Restart NinjaTrader** - Often fixes quirky behavior


## Quick Reference Card

```
┌─────────────────────────────────────────────────────┐
│         DRAG-DROP BRACKET TOOL - QUICK REF          │
├─────────────────────────────────────────────────────┤
│ 1. Enter position via Chart Trader                  │
│ 2. Click "Bracket Tool: OFF" → turns GREEN          │
│ 3. Click and DRAG on chart to target price          │
│ 4. Release mouse → orders placed                    │
│ 5. Tool auto-disables (button turns RED)            │
├─────────────────────────────────────────────────────┤
│ LONG: Drag down = SL, Drag up = TP                  │
│ SHORT: Drag up = SL, Drag down = TP                 │
│                                                      │
│ Yellow line = preview                               │
│ Green button = enabled                              │
│ Red button = disabled                               │
└─────────────────────────────────────────────────────┘
```

## Version History

**v1.0** - Initial release
- Basic drag-and-drop functionality
- OCO bracket orders
- Toggle button interface
- Automatic mirroring
- Auto-disable safety feature

## Credits

Developed for BadBuddha Customs
Requested by UncleRogerski

---

**Happy Trading! 📈**

*Remember: Always test on a Sim account first before using with real money.*
