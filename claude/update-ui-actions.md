# ui-actions.md

The file `src/SmartGit/Manual/ui-actions.md` serves as a **comprehensive index** of all available menu items in SmartGit.

- The list is organized by **window style** (_Standard_, _Log_, and _Working Tree_ windows).  
- Each relevant menu item must be listed and linked to the most appropriate page in the Manual.  
- The following types of items should **not** be included:  
  - Trivial items (e.g., `Exit`)  
  - Debug-related items  

## Updating `ui-actions.md`

Use `.temp/ui-map.tsv` as the source for new menu items. For each entry:

### 1. Decide if the item should be listed
- If **trivial** or **debug-related**, **do not list it**.  
- Instead, add it to `.temp/ui-map-ignored.txt` with:  
  - `windowKey`  
  - `controlText`  
  - `controlId` (if present)  

  to ensure the item is uniquely identified.

### 2. If the item should be listed
- Confirm it is **not already in** `.temp/ui-map-ignored.txt` or `.temp/ui-map-processed.txt`.  
- If not contained in either of these files, add it to `ui-actions.md` using these rules:
  - Use `windowTitle` and `windowKey` to determine the correct window section.  
  - **Remove** `...` from the `controlText` if present.  
  - If the meaning could be unclear, **add clarifying info in parentheses** directly after the control text:  
    - Example:  
      - `Push (commits)`  
      - `Push (subtrees)`  
  - If available, **include `controlDetails`**.  
- After adding, record the item in `.temp/ui-map-processed.txt` with:  
  - `windowKey`  
  - `controlText`  
  - `controlId` (if present)  

This prevents duplicates and ensures traceability.  
