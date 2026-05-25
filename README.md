# Bathys

Bathys is a first-person boomer shooter prototype built in Unreal Engine 5 using Blueprints only. Set in a dystopian underwater city where coral mutations have spread to human brains, the game draws aesthetic inspiration from BioShock, The Last of Us, and Fallout. The player controls a survivor navigating flooded corridors armed with a pump-action shotgun, fighting off coral-infected enemies. Core systems include a fully functional shotgun with spread, fire rate, and reload mechanics, a circular HUD health bar rendered through a custom UMG material, an ammo pip display, Blueprint Interface-driven health and ammo pickups, camera recoil, and a sprite-based weapon animation system. The project is a work-in-progress prototype developed for a game jam.

## What's Built

**Core Character**
- BP_ReefCharacter — movement, look, sprint, health, damage, death
- Enhanced Input — move, look, jump, fire, sprint all wired

**Weapon**
- BP_Shotgun — fires 8 pellets via line trace, 2 shell ammo, fire rate cooldown, reload, recoil (camera pitch kick)
- bFired fix — animation and UI only trigger on actual shots, not on empty clicks

**UI**
- Circular health bar — M_CircularBar material, WBP_HP, wired through WBP_MainUI
- Ammo pips — WBP_AmmoPips, updates on fire and reload
- WBP_Weapon — sprite animation system fully built (fire + reload anims) but currently disconnected

**Pickups**
- BPI_Pickup interface — RefillAmmo + RefillHealth (no cast system)
- BP_AmmoPickup — refills to MaxAmmo, destroys self
- BP_HealthPickup — refills to MaxHealth, destroys self
