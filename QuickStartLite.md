# Bracket Manager LITE - Quick Start

**Get trading in 2 minutes!** | Simplified Version

---

## What is LITE?

LITE is the **simplified version** with:
- ✅ Fixed 1:2 Risk:Reward ratio (most popular)
- ✅ Drag-and-drop interface
- ✅ Simple one-button operation
- ✅ Breakeven buttons (BE+1, BE+5) **NEW in v2.3.0**
- ✅ 10-tick trailing stop **NEW in v2.3.0**
- ✅ No configuration needed
<<<<<<< HEAD
- ✅ User-based license
=======

>>>>>>> 06e7bff2d5ebc82d491521acdf49f9e3f62580fc

**Want more?** Upgrade to PRO for custom ratios, hotkeys, overlay, scaling, and more!

---

## Installation (30 seconds)

1. Open NinjaTrader 8
2. **Control Center → Tools → Import → NinjaScript Add-On**
3. Select the LITE `.zip` file → **Import**
4. Press **F5** (Compile)
5. **Restart NinjaTrader**

Done! ✓

---

## First Trade (90 seconds)

### Step 1: Setup
- Open any chart
- Press **Ctrl+T** to enable Chart Trader
- Look for **"Bracket LITE: OFF (1:2)"** button at bottom

### Step 2: Enter Position
- Use Chart Trader to go Long or Short
- Must have active position for tool to work

### Step 3: Place Brackets
1. Click **"Bracket LITE: OFF"** → turns green "ON"
2. **Drag on chart**:
   - **LONG**: Drag DOWN for SL (TP auto-calculates) or UP for TP (SL auto-calculates)
   - **SHORT**: Drag UP for SL (TP auto-calculates) or DOWN for TP (SL auto-calculates)
3. Watch yellow line as you drag
4. **Release** → Orders submit immediately

Tool automatically turns OFF after placing orders.

---

## Position Management (NEW in v2.3.0)

After placing your brackets, you now have **three powerful buttons** for managing your position:

### BE +1 Button
- **What it does**: Moves your stop loss to **breakeven + 1 tick**
- **When to use**: Lock in a tiny profit once price moves in your favor
- **How it works**: Click button → Stop moves to entry price + 1 tick instantly
- **Example**: Long ES @ 4500 → Price reaches 4515 → Click BE+1 → Stop moves to 4500.25

### BE +5 Button
- **What it does**: Moves your stop loss to **breakeven + 5 ticks**
- **When to use**: Lock in small profit with more breathing room
- **How it works**: Click button → Stop moves to entry price + 5 ticks instantly
- **Example**: Long ES @ 4500 → Price reaches 4520 → Click BE+5 → Stop moves to 4501.25

### Trail 10 Button
- **What it does**: Enables a **10-tick trailing stop** that follows price
- **When to use**: Let winners run while protecting gains
- **How it works**:
  - Click button (turns green when active)
  - **LONG**: Stop moves UP as price rises (stays 10 ticks below highest price)
  - **SHORT**: Stop moves DOWN as price falls (stays 10 ticks above lowest price)
  - Stop ONLY moves in favorable direction (never worse)
  - Auto-disables when position closes
- **Example**:
  - Long ES @ 4500
  - Click Trail 10 → Stop starts at 4490 (10 ticks below current)
  - Price rises to 4530 → Stop moves to 4520 (10 ticks below)
  - Price drops to 4525 → Stop stays at 4520 (doesn't move down!)
  - Stopped out at 4520 for +20 point profit

**Pro Tip**: Combine these tools! Use BE+1 early, then Trail 10 when you have more profit cushion.

---

## Example: Long at ES 4500

You're **long ES at 4500** and want to set brackets with 1:2 ratio:

**Method 1 - Drag to set Stop Loss**:
- Click button (turns green)
- Drag DOWN to 4490
- Release
- ✓ Result: SL @ 4490, TP @ 4520 (10 risk, 20 reward)

**Method 2 - Drag to set Take Profit**:
- Click button (turns green)
- Drag UP to 4520
- Release
- ✓ Result: SL @ 4490, TP @ 4520 (10 risk, 20 reward)

**Both methods work!** Use whichever feels natural.

---

## The 1:2 Ratio

LITE uses a **fixed 1:2** risk:reward ratio:

| You Risk | You Target | Ratio |
|----------|------------|-------|
| 10 points | 20 points | 1:2 |
| $50 | $100 | 1:2 |
| 5 ticks | 10 ticks | 1:2 |

**Why 1:2?**
- Most popular among professional traders
- Win rate of 35%+ breaks even
- Balanced approach: not too conservative, not too aggressive
- Proven over decades of trading

**Want different ratios?** → [Upgrade to PRO](https://badbuddhatrades.com)

---

## Quick Reference

### Main Toggle Button States
- **Red "OFF"** → Tool disabled, won't respond to drags
- **Green "ON"** → Tool active, ready to place brackets
- **(1:2)** → Current ratio (fixed in LITE)

### Position Management Buttons (NEW)
- **BE +1** (Gray) → Click to move stop to breakeven + 1 tick
- **BE +5** (Gray) → Click to move stop to breakeven + 5 ticks
- **Trail 10** (Brown/Green) → Click to enable 10-tick trailing stop
  - Brown = Inactive
  - Green = Actively trailing
  - Auto-disables when position closes

### Drag Directions

**LONG Positions**:
- Drag DOWN → Sets Stop Loss (TP calculated)
- Drag UP → Sets Take Profit (SL calculated)

**SHORT Positions**:
- Drag UP → Sets Stop Loss (TP calculated)
- Drag DOWN → Sets Take Profit (SL calculated)

### Visual Cue
- **Yellow dashed line** → Shows your drag level in real-time

---

## Common Questions

**Q: Nothing happens when I drag?**
- ✓ Is button GREEN (ON)?
- ✓ Do you have an active position?
- ✓ Are you dragging in the price area (not indicator panel)?

**Q: Can I change the 1:2 ratio?**
- No, LITE is simplified. Upgrade to PRO for 6 ratios (1:1, 1:2, 1:3, 2:1, 3:1, Custom).

**Q: Can I place multiple bracket sets?**
- No, LITE places one set. Upgrade to PRO for position scaling (e.g., 50% @ 1:1, 30% @ 1:2, 20% @ 1:3).

**Q: Are there hotkeys?**
- No, LITE is click-only. PRO adds Ctrl+Shift+B (toggle) and Ctrl+Shift+R (cycle ratios).

**Q: Where are the settings?**
- LITE has no settings (keeps it simple!). PRO has a full settings window with 5 tabs.

<<<<<<< HEAD
**Q: Does LITE require a license?**
- Yes, LITE requires a user-based license tied to your NinjaTrader account.

=======
>>>>>>> 06e7bff2d5ebc82d491521acdf49f9e3f62580fc
**Q: When should I use BE+1 vs BE+5?**
- Use BE+1 early when price just starts moving in your favor (more conservative)
- Use BE+5 when you have more profit cushion and want breathing room (less likely to get stopped out on minor retracements)

**Q: Can I change the trailing stop from 10 ticks?**
- No, LITE uses a fixed 10-tick trailing stop. Upgrade to PRO for configurable trailing amounts and ATR-based trailing.

**Q: Does the Trail 10 button work with any position size?**
- Yes! The trailing stop works with any position size and any instrument.

**Q: What happens to my brackets if I hit the REVERSE button?**
- ⚠️ **CRITICAL**: The bracket orders (SL/TP) are NOT automatically canceled when you reverse your position!
- The old orders remain active and can cause unintended fills
- **ALWAYS manually cancel bracket orders before reversing**
- Example problem: You're LONG with SL/TP set → You reverse to SHORT → Old orders still active → Can add to position instead of exiting
- **Best practice**: Cancel all working orders before using the reverse function

---

## Tips for Success

### Before Trading Live
1. ✓ Test in **Sim account** first
2. ✓ Practice Long and Short drag directions
3. ✓ Get comfortable with the workflow
4. ✓ Verify orders appear correctly in Chart Trader

### During Trading
1. ✓ Enter position first
2. ✓ Immediately click button to turn ON
3. ✓ Watch yellow line to confirm your drag level
4. ✓ Release when ready
5. ✓ Verify brackets appeared on chart
6. ✓ Use BE+1/BE+5 to lock in profits as price moves in your favor
7. ✓ Enable Trail 10 to let winners run while protecting gains
8. ✓ **If reversing position: Cancel all working orders FIRST, then reverse**

### Avoid These Mistakes
- ❌ Dragging the wrong direction for your position type
- ❌ Forgetting to turn tool ON (button must be green)
- ❌ Leaving tool ON when not using it
- ❌ Placing brackets before entering position
- ❌ **Using the REVERSE button without canceling bracket orders first** (CRITICAL!)
- ❌ Assuming brackets auto-cancel when position closes via reverse

---

## What You're Missing (PRO Features)

LITE v2.3.0 now includes breakeven and trailing stops, but PRO gives you even more:

### 1. Multiple Ratios
- 1:1, 1:2, 1:3, 2:1, 3:1, Custom
- Switch between them instantly

### 2. Real-time Overlay
```
R:R: 1:2
Entry: 4500.00
→ SL: 4490.00 (-10.00)
  TP: 4520.00 (+20.00)
```
See exact prices BEFORE releasing!

### 3. Hotkeys
- **Ctrl+Shift+B** → Toggle on/off (no clicking!)
- **Ctrl+Shift+R** → Cycle ratios

### 4. Position Scaling
One drag creates multiple targets:
- 50% exits @ 1:1 (lock in profits)
- 30% exits @ 1:2 (main target)
- 20% exits @ 1:3 (let it run)

### 5. Advanced Trailing Stops
- Configurable trailing tick amounts (not just 10)
- Multiple trailing strategies
- ATR-based trailing

### 6. Sound Alerts
- Success sound when orders place
- Error sound if something fails
- Cycle sound when changing ratio

### 7. Settings Window
Full control over everything:
- Overlay position
- Sound volume
- Bracket set configuration
- Trailing stop settings
- Debug logging

**[→ Learn more about PRO](../PRO/README.md)**

---

## Troubleshooting

### Orders didn't place
1. Check you have account selected in Chart Trader
2. Verify drag direction matches position type
3. Make sure you have active position
4. Confirm you dragged far enough (>2 pixels)

### Unexpected order fills after reversing
1. **This happens if you reversed without canceling brackets first**
2. Old SL/TP orders remain active and can fill against your new position
3. **Solution**: Right-click chart → Cancel All Orders
4. **Prevention**: ALWAYS cancel working orders before using reverse button

### Wrong prices
- LITE always uses 1:2 ratio, no exceptions
- Check your position direction (Long vs Short)
- Verify entry price in Chart Trader

### Button won't turn ON
1. Make sure Chart Trader is open (Ctrl+T)
2. Restart NinjaTrader
3. Recompile (F5 in Control Center)

---

## Ready to Upgrade?

### PRO is for you if:
- ✅ You want to use ratios other than 1:2
- ✅ You trade multiple strategies needing different ratios
- ✅ You want to scale out of positions
- ✅ You prefer keyboard hotkeys
- ✅ You want visual confirmation before placing
- ✅ You need configurable trailing stops (not just 10 ticks)

### LITE v2.3.0 is enough if:
- ✅ 1:2 ratio works for your strategy
- ✅ You only need single brackets
- ✅ You don't mind clicking the button
- ✅ You trust your drag placement
- ✅ 10-tick trailing stop meets your needs
- ✅ Breakeven buttons give you enough control

**No wrong choice!** Both versions use the same core drag logic.

**[→ Get PRO Version](https://badbuddhatrades.com)**

---

## Next Steps

1. ✓ Practice in Sim account
2. ✓ Try both drag methods (setting SL vs setting TP)
3. ✓ Experiment with BE+1, BE+5, and Trail 10 buttons
4. ✓ Verify the 1:2 ratio matches your strategy
5. ✓ Test trailing stop behavior in different market conditions
6. ✓ Consider upgrading if you need more flexibility

**Happy trading!** 🎯

---

**Support**: support@badbuddhatrades.com | **Website**: https://badbuddhatrades.com

**Version**: 2.3.0 | **© 2025 BadBuddha Customs LLC**
