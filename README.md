# EFTH Weapon Sway Compatibility

A compatibility mod that integrates **EFT Health System (EFTH)** with **Weapon Sway** to provide realistic weapon handling penalties based on arm health status.

## 🎯 Features

- **Dynamic Weapon Sway**: Weapon sway intensity changes based on your arm health
- **Realistic Health Penalties**: Injured arms affect weapon stability realistically
- **Asymmetry Penalties**: Different damage levels between arms create additional sway
- **Destroyed Limb Support**: Severe penalties when arms are completely destroyed
- **Fully Configurable**: Extensive MCM options to customize all aspects

## 📋 Requirements

### Essential
- **S.T.A.L.K.E.R. Anomaly** (1.5.3)
- **[EFT Health System (EFTH)](https://discord.com/channels/456765861953536020/1248756352881266772)** by vegeta1k95, Lizzardman, Lasie, Fabio Conte, Joe, Joker Burger, MrShersh
- **[Weapon Sway](https://www.moddb.com/mods/stalker-anomaly/addons/weapon-sway)** by bvcx
- **[MCM (Mod Configuration Menu)](https://www.moddb.com/mods/stalker-anomaly/addons/anomaly-mod-configuration-menu)** by ravenascendant
- **[Modded executable](https://github.com/themrdemonized/xray-monolith)** by themrdemonized

## 🚀 Installation

### Mod Organizer 2 (Recommended)
1. Download the latest release
2. Install through MO2's "Install Mod" feature
3. Ensure load order: `EFTH` → `Weapon Sway` → `EFTH Weapon Sway Compatibility`
4. Launch the game and configure via MCM

### Manual Installation
1. Extract the archive
2. Copy the `gamedata` folder to your Anomaly installation directory
3. Merge folders when prompted
4. Launch the game

## ⚙️ Configuration

Access settings through **MCM → EFTH Weapon Sway**

### Health Thresholds
Configure when different sway penalties activate:
- **Excellent Health**: 90%+ arm health (minimal sway)
- **Good Health**: 70-90% arm health (light sway increase)
- **Moderate Health**: 50-70% arm health (moderate sway)
- **Heavy Damage**: 30-50% arm health (significant sway)
- **Severe Damage**: 1-30% arm health (severe sway penalties)

### Sway Power Settings
Fine-tune sway intensity for each health range:
- **Base Power**: Starting sway value for each health tier
- **Multipliers**: How quickly sway increases as health decreases

### Penalty Systems
- **Asymmetry Penalty**: Extra sway when one arm is much more damaged
- **Destroyed Limb Multipliers**: Additional penalties for destroyed arms

## 🎮 How It Works

### Health-Based Sway Calculation
The mod calculates weapon sway based on:

1. **Average Arm Health**: Takes the mean HP of both arms
2. **Health Tier Assignment**: Determines which sway category applies
3. **Progressive Scaling**: Sway increases smoothly within each tier
4. **Asymmetry Check**: Adds penalties for uneven arm damage
5. **Destruction Bonuses**: Severe penalties for destroyed limbs

### Example Scenarios
- **100% arm health**: Minimal sway (0.2 power)
- **75% arm health**: Light sway increase (0.4 power)
- **45% arm health**: Moderate sway (1.0 power)
- **15% arm health**: Heavy sway (2.5 power)
- **One destroyed arm**: +20% sway penalty
- **Both destroyed arms**: +40% sway penalty

## 🔧 Compatibility

### Known Compatible Mods
- G.A.M.M.A

## 🐛 Troubleshooting

### Common Issues

**Q: Weapon sway not working**
- Ensure EFTH patch is enabled in MCM
- Verify both EFTH and Weapon Sway mods are installed
- Ensure Weapon Sway is enabled in MCM

**Q: Settings not applying**
- MCM changes apply in real-time
- Try toggling debug mode to verify calculations

### Debug Mode
Enable debug mode in MCM to see:
- Current arm health percentages
- Applied sway multipliers
- Final sway calculations

## 🤝 Credits

- **Dr_Cox1911**: Mod development and integration
- **vegeta1k95, Lizzardman, Lasie, Fabio Conte, Joe, Joker Burger, MrShersh**: EFT Health System
- **bvcx**: Original Weapon Sway mod
- **S.T.A.L.K.E.R. Modding Community**: Support and feedback

---

*Made with ❤️ for the S.T.A.L.K.E.R. community*