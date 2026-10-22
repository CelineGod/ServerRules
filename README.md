# ServerRules 📜

A lightweight, customizable Minecraft plugin (Spigot/Paper 1.20+) that opens an interactive rules GUI when players run the `/rules` command.

---

## 🌟 Features
- **Interactive GUI Menu:** Clean 3-row inventory layout displaying server rules.
- **Commands & Aliases:** Access the menu via `/rules`, `/rule`, or `/rulebook`.
- **Item Protection:** Prevents players from taking, moving, or dragging items out of the GUI.
- **Zero Dependencies:** Built purely with the standard Spigot/Paper API.

---

## 📖 Default Rule Categories
1. 💬 **Chat Rules:** Respect, no spam, no advertising.
2. ⚔️ **Hacks & Cheating:** No hacked clients, X-Ray, bug exploits, or screen share refusal.
3. 🚫 **Severe Violations:** Real World Trading (RWT), DoS/doxxing threats, and account phishing (leads to permanent blacklist).

---

## 🛠️ How to Customize the Plugin

If you want to edit the rules, change the items, or customize the GUI layout to fit your server, you can easily modify the `ServerRules.java` file before building the JAR.

### 1. Changing Item Materials & Positions
In `ServerRules.java`, inside the `openRulesGUI` method, you can change the item slots and materials:

```java
// Slot positions (0 to 26 for a 27-slot inventory)
gui.setItem(11, chatItem);       // Middle of 2nd row (Left)
gui.setItem(13, hackItem);       // Middle of 2nd row (Center)
gui.setItem(15, blacklistItem);  // Middle of 2nd row (Right)

// Material examples
ItemStack chatItem = new ItemStack(Material.BOOK); // Change Material.PAPER to Material.BOOK
