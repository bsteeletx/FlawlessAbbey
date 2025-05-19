# Inventory Pickup Prototype

## Overview

This Unreal Engine project demonstrates a basic first-person inventory pickup system. The player can walk around, look around, and pick up items scattered in the world. An inventory UI displays the items as they are collected. A preview system exists but is not yet fully integrated.

---

## Features

- **First-Person Controls**:  
  - Movement and camera look are fully implemented.
- **Item Pickup**:  
  - Walk up to an item and pick it up.
  - Picked-up items are added to the inventory.
- **Inventory UI**:  
  - Shows collected items in slots as they are picked up.
  - UI refresh is triggered on item pickup.
- **Preview System**:  
  - Preview logic is set up but not currently tied into active gameplay/UI.
- **Code Structure**:  
  - Inventory widget is created in the player character blueprint.
  - Inventory logic and UI update logic are separated.

---

## Known Issues

- **Slot Wiping Bug**:  
  - When picking up the 2nd item, slot 1 is cleared.
  - When picking up the 3rd item, slot 2 is cleared, and so on.
  - This appears to be a bug in the logic that updates or assigns inventory slots on pickup.
- **UI Refresh**:  
  - UI refreshes as intended on each pickup, but inventory slot logic needs review.
- **Preview System**:  
  - Exists in code but is not currently triggered or visible in the UI.

---

## Usage

1. **Launch the project in Unreal Engine.**
2. **Play in Editor (PIE).**
3. **Walk around using WASD + Mouse.**
4. **Approach items and pick them up.**
5. **Observe inventory UI updating.**

---

## Suggestions for Reviewers

- Review the logic that assigns items to inventory slots; specifically, check for array index handling or slot-clearing logic when multiple items are collected.
- Check for any off-by-one or overwrite issues in the inventory array or UI update code.
- Consider reviewing/refactoring the preview system to connect it to the UI for a better player experience.
- Test edge cases: picking up more items than slots, picking up/dropping in quick succession, etc.

---

## Additional Notes

- The inventory widget is referenced and created in the player character blueprint.
- UI update function (`RefreshInventoryUI`) is called after each pickup.
- All code and Blueprints should be easy to follow for the purposes of this prototype.
- The project is still a work-in-progress; feel free to expand, refactor, or connect the preview system as needed.

---

## Author Notes

- This prototype represents several hours of iteration, testing, and debugging.
- The known slot-wiping issue was the last major blocking bug.  
  Reviewer insight on this would be appreciated!
- If you have any questions or suggestions, please leave comments in the code or Blueprint nodes.

---

Thank you for reviewing!
