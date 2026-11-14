# WoW Imito 1.5.4

## Graphics and performance

- Fixed Vulkan frame synchronization and graphics-resource handling that could freeze the login screen or game while audio continued.
- Fixed stale graphics textures after a rendering surface was recreated.
- Improved Vulkan selection and recovery on eligible Mali devices while retaining graphics capability checks.
- Classic clients now choose a lighter starting resolution on devices with less RAM. Existing graphics settings are preserved.
- Reduced unnecessary Touch UI geometry checks and background chat processing.

## Touch UI

- Added a movable Map button, matching the size of the Bags, Game Menu and Chat buttons.
- Restored the Map toolbar in Forever, including Zoom in, Zoom out, Reset and Close.
- Improved the fit and readability of Talents and other game windows.
- Updated the Map, Game Menu, Chat, Sheathe Weapon and Bags icons with a consistent design.
- Improved the default control layout, including Walk/Run and Sheathe Weapon on the bottom edge. Controls stay aligned when the resolution changes.
- Completed missing translations in Touch UI controls, layout settings, spell slots and inventory actions across all supported languages.
- Fixed controls disappearing while dead, near a corpse or at instance entrances.

## Reports

- Added clearer graphics probe and startup diagnostics to exported reports.
- Preserved automatic report submission when the report service uses an older diagnostics format.
- Fixed stale launch diagnostics and mismatched settings in problem reports.
