# 🎖️ Custom Rank Icons Resource Pack for Minecraft 🎖️

This simple resource pack allows you to replace **specific Unicode characters with custom images**, making it easy to display **custom ranks or icons** in Minecraft chat, tab list, or anywhere text is rendered! 🏆

---

## ✨ Features
- Display **custom rank icons** next to player names in chat or tab list.
- Supports **unused Unicode characters** to avoid conflicting with normal text.
- Lightweight and optimized for Minecraft **1.21.x** (but works on most modern versions).

---

## ⚠️ Client Requirement
> 📝 **Players MUST have the resource pack loaded on their client** to see the icons!

### 👉 Server-Side Enforcement:
To automatically prompt players to download the pack, you can set a **resource-pack URL** in your server `server.properties`:

🔌 Recommended Fabric Mod:
📦 Resourcepack Organizer (1.21.x)

    Allows automatic server resource pack downloading.
    Lets players manage server-suggested packs more easily.
    You can configure it to force-load or prompt users to accept the pack when connecting.

Alternatively:

    Custom Pack Loader (for Fabric)
        It allows servers to distribute custom resource packs automatically, very useful for modded servers!

Or use plugins like **[Server Resource Pack Loader](https://www.spigotmc.org/resources/81208/)** to manage resource packs dynamically!


---

## 🚀 How to Use

1. **Install the resource pack** on your server or client as you would any other pack.
2. In your Minecraft plugin/mod (e.g., LuckPerms, StyledChat, Essentials, etc.), use the special Unicode characters (see list below) where you want the icons to appear. Example:
  -  LuckPerms
    /lp creategroup admin
    /lp group admin meta addprefix 100 "⍡"

The ⍡ will be replaced with your custom image!

---

## 🛠️ How to Customize for Your Server

1. **Unzip** the M2CRI zip file

2. **Add your custom image**:
- Place your image file (e.g., `admin_rank.png`) into:
  ```
  assets/minecraft/textures/ranks/
  ```
- Recommended size: **8x9 px** or **16x18 px** for best quality.

2. **Edit the character mapping**:
- Open:
  ```
  assets/minecraft/font/default.json
  ```
- Find the Unicode character entry you want to use (e.g., ⍡) and change the `"file"` to the name of your image:
  ```json
  {
    "type": "bitmap",
    "file": "minecraft:textures/ranks/mod_rank.png",
    "ascent": 8,
    "height": 16,
    "chars": ["⍡"]
  }
  ```

3. **Save & rezip** the pack! 🎉

---

## 🔠 Recommended Unused Characters

Here are some Unicode characters Minecraft typically does not use, so they are safe for custom icons:

| Character | Unicode |
|-----------|---------|
| ⍡         | U+2351  |
| ⍛         | U+235B  |
| ⍢         | U+2352  |
| ⍜         | U+235C  |
| ⍖         | U+2356  |
| ⍕         | U+2355  |
| ⍙         | U+2359  |
| ⍝         | U+235D  |
| ⍞         | U+235E  |


Feel free to pick any **obscure Unicode symbols** that won't interfere with regular text!
(https://www.compart.com/en/unicode)
---

## 🖼️ Screenshots
Example with ![Styled Player List](https://www.curseforge.com/minecraft/mc-mods/styled-player-list) & ![Styled Chat](https://www.curseforge.com/minecraft/mc-mods/styled-chat): -->
![Owner_msg](https://github.com/user-attachments/assets/a5f7f936-0384-4a0b-9f05-7a841d92c9dc)
<img src="https://github.com/user-attachments/assets/66d85741-b1b2-4f2e-969a-6e0b47923291" alt="Owner Tab" width="400" height="300">
<img src="https://github.com/user-attachments/assets/037d1a9d-d70f-468a-a905-175d33fad054" alt="Owner Tab" width="400" height="300">


---

## 💡 Notes
- This will only work if the CLient has the Resourcepack loaded. For this you can use some mods or plugins
- Make sure the font file includes **all your custom characters**.
- For **animated icons**, you can also use `.mcmeta` animation files alongside your textures.
- Works great with popular chat formatting plugins like **LuckPerms**, **StyledChat**, or **TAB**!

---

🎉 Enjoy your custom ranks and make your server stand out! 🚀

