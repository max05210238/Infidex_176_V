# Infidex 176 V

Open source 3D printed panoramic 35mm film camera. Shoots a 3:1 panoramic frame (72 x 24 mm) on standard 35mm film using a Mamiya TLR taking lens.

Designed by **Denis Aminev** (Time to Waste). This repository is a community mirror created to preserve the project after the original site goes offline. See [Source and license](#source-and-license).

---

## Download

**Want everything in one file?** Download [`Infidex_176_V_complete.zip`](downloads/Infidex_176_V_complete.zip) (~20 MB) — this is the author's original release archive containing all STL, FBX, MOD files, the PDF manual, and the 3ds Max source. Just unzip and print.

You can also clone the full repo:

```bash
git clone https://github.com/max05210238/Infidex_176_V.git
```

Or use GitHub's **Code > Download ZIP** button above to grab the entire repository (docs included).

---

## What this is

Infidex 176 V is a fully working camera you print on an FFF/FDM printer and finish by hand. It is a plastic camera, so tolerances depend heavily on your printer, filament, and finishing. Expect to iterate. The designer printed all his cameras on a stock Ender 3 (Marlin firmware, Linear Advance) in cheap ABS.

| Spec | Value |
|---|---|
| Format | 3:1 panoramic, 72 x 24 mm |
| Film | 35mm (135) |
| Frames per 36-exp roll | 18 (19 if loaded in full dark, no leader waste) |
| Sprockets per frame | 16 (two standard 3:2 frames wide) |
| Taking lens | Mamiya TLR (C2/22/220, C3/33/330). 80mm recommended |
| Equivalent focal length | ~35mm on the 72mm-wide panoramic frame |
| Infinity focus (Mamiya 80mm) | ~31 m (~102 ft), helicoid fully screwed in |
| Focus throw | ~300 deg from infinity to 2 m |
| Body length | 168 mm |
| Body height (unibody) | 67 mm |
| Body thickness | 37.8 mm |
| Filament per camera | < 600 g (22 oz) |
| Tripod mount | 1/4" brass insert in base (8 x 8 mm) |

---

## Repository contents

```
Infidex_176_V/
├── Infidex 176 V manual.pdf         Original PDF manual by Denis Aminev
├── Infidex 176 V_NEWEST.max         3ds Max master CAD source file
├── STL/                              Print-ready STL parts
│   ├── Body/                           Body shells, unibody, doors (10 files)
│   ├── Lens mount/
│   │   ├── Focusing Helicoid/          Helicoid parts inc. Blue Dot variants (15 files)
│   │   ├── Classic Cone/               Fixed cone mount (3 files)
│   │   ├── Tube/                       Tube mount (3 files)
│   │   └── Old Version cone for T-22 lens/  Legacy T-22 cone (4 files)
│   └── Small parts/                    Knobs, gears, viewfinders, lens hoods, etc. (25 files)
├── FBX/                              FBX mesh exports (62 files)
├── MODS/                             Community modifications
│   ├── stl/                            Modified body, doors, helicoid mount (7 files)
│   └── fbx/                            FBX versions of the mods (7 files)
├── downloads/
│   └── Infidex_176_V_complete.zip    Author's original release archive (~20 MB)
├── docs/
│   ├── PRINTING.md                   Part catalog, print settings, dimensions
│   ├── ASSEMBLY.md                   Step-by-step build (14 steps)
│   ├── FOCUSING_AND_USAGE.md         Focus calibration, DOF table, shooting, scanning
│   └── VIDEO_TRANSCRIPT.md           Transcript of the designer's build video
├── NOTICE.md                         Attribution and redistribution notice
└── README.md                         This file
```

> If you regenerate STLs from `Infidex 176 V_NEWEST.max`, keep the part names above so the assembly docs stay valid.

---

## Required materials and tools

| Item | Notes |
|---|---|
| Mamiya TLR taking lens | C2/22/220 or C3/33/330. 80mm is the recommended focal length |
| Filament, 1 roll | Whole camera is under 600 g. ABS, PLA, or PETG all work (see notes below) |
| Superglue | Two-component with activator preferred. Standard CA works |
| Rigid wire, 0.6 to 0.8 mm | 20 to 30 cm. Stainless steel. Must spring well |
| Black flocked self-adhesive paper or matte black vinyl | Light-trap and anti-reflection surfaces |
| Black foam (dark gray minimum) | Light seals and film tension shims |
| Double sided tape | Not foam based |
| Wire nippers | |
| Calipers, metric | For dimension checks |
| Sandpaper, 100P to 800P | Grit depends on your filament |
| Spanner wrench | For the Mamiya lens mount nut |
| Scissors, tweezers | |
| Safety goggles + respirator | Mandatory for ABS fumes and superglue |

### Optional

35mm optical viewfinder, cutting knife with replaceable blades, 3D-print bed adhesive (spray), epoxy, plastic putty, 1000P fine sandpaper, textured bumper paint (e.g. Mipa), brass heat inserts (1/4" 8x8 mm and M3 4.5x6 mm), four or more M3x10 screws, soldering iron.

### Filament notes

ABS is the designer's choice: cheap, easy to shape by hand, good mechanical properties, but it shrinks, needs bed adhesive, slow speeds (30 to 70 mm/s), and an enclosed chamber. PLA works fine (tested by a friend of the designer). PETG can be too flexible in some parts. Composite filaments hide print lines well but are expensive and not every printer handles them.

---

## Print settings (designer's ABS profile)

| Setting | Value |
|---|---|
| Nozzle | 0.4 mm |
| Layer height | 0.2 mm |
| First layer height | 0.23 mm (glass bed) |
| Inner perimeters | 4 (important for rigidity) |
| Min top/bottom thickness | 2 mm |
| Infill | 25% max |
| Bed | 4 mm polished glass (PEI also fine) |

Print order does not matter, but print the **body first** to verify dimensions and tolerance before committing the rest. Reasonable deviation of 0.2 to 0.4 mm on printed parts is fine. See [docs/PRINTING.md](docs/PRINTING.md) for the full part catalog and per-part orientation.

---

## Build at a glance

Full walkthrough in [docs/ASSEMBLY.md](docs/ASSEMBLY.md).

1. Check body dimensions (37.8 mm thickness, 36.03 mm reference height).
2. Glue or screw the lens mount to the body. Install brass inserts if used.
3. Build the lens mount: lens board to inner thread, snap fixation ring, glue focus ring to the fixation ring (not the mount), verify the thread screws all the way in.
4. Install spool base, taking spool shaft, sprockets gear and sprocket shaft.
5. Bend the V-spring from wire, install it and the rewind knob.
6. Hinge the door with a ~63 mm wire pin. Line the pressure plate with black flock and add 4 to 5 mm foam tension strips.
7. Cold shoe, optional cable release port and lever knob, optional lens hood.
8. Calibrate the focus marks against ground glass (see [docs/FOCUSING_AND_USAGE.md](docs/FOCUSING_AND_USAGE.md)).

Wear eye and respiratory protection throughout. Glue fumes will make your eyes water.

---

## Lens mount options

Print only one set:

- **Focusing helicoid** (recommended, allows real focusing)
- **Classical cone** (fixed)
- **Tube mount** (fixed)

The lens cone from the previous IV model is compatible. All three are available with M3 screw holes.

**Blue Dot lens owners:** Blue Dot copies of the 80mm have a different flange distance and will not reach infinity with the standard helicoid. Print the shorter parts instead: `Helicoid_INNER_ring_80mm_shorter-2mm.STL` and `Helicoid_FOCUS_ring_ribs_shorter-2mm.STL`.

---

## Flocking paper templates

| Size | Location |
|---|---|
| 73 x 23 mm | Top and bottom of film chamber |
| 43 x 23 mm | Sides of film chamber |
| 82 x 33 mm | Pressure plate |

---

## Known limitations

- The frame counter requires **2 revolutions per shot** with the stock 8-tooth sprocket gear. A 16-tooth gear fixes this but lengthens the body.
- Long panoramic negatives are hard to scan at a normal lab. The designer scans on an Epson V850 Pro, or DSLR-scans and stitches two frames.

---

## Credits

Project by **Denis Aminev**, Time to Waste.

- **PaperBen** and **Giuseppe Spataro** for testing, advice, and inspiration. Giuseppe also solved the Blue Dot infinity issue.
- **ballanux** (YouTube) for helicoid system inspiration.
- **Oscar Oweson**, creator of the Oxygen panoramic camera (panomicron.com), for inspiration on some parts.
- **GLOwl** for the printable lens cap that inspired the kit version.
- **@analog_astronaut** for boosting the project.

---

## File sources

All design files in this repository originate from Denis Aminev's official releases on [timetowaste.ru](https://timetowaste.ru). The files were downloaded directly from the author's site before the scheduled shutdown.

| Path | Source | Notes |
|---|---|---|
| `Infidex 176 V manual.pdf` | Author's site, unchanged | The original PDF assembly and printing guide |
| `Infidex 176 V_NEWEST.max` | Author's site, unchanged | 3ds Max master CAD — regenerate STLs from this |
| `STL/` | Author's site, unchanged | Print-ready parts exported by the author |
| `FBX/` | Author's site, unchanged | Mesh exports for viewing/editing in other 3D tools |
| `MODS/` | Author's site, unchanged | Community-contributed body and door variants |
| `downloads/Infidex_176_V_complete.zip` | Author's original release archive | All binary files in one download (~20 MB) |
| `docs/` | Written for this mirror | English documentation reorganized from the PDF manual and the author's build video for easier web reading |

No design files have been modified. The documentation in `docs/` is a reorganization of the author's own content into Markdown for web readability.

---

## Source and license

Original project, files, and documentation by Denis Aminev (Time to Waste).

The designer's original site is shutting down. His own words:

> This website will disappear on 21 March 2027. Project brought to a point where I am satisfied with the results and I will no longer pay for this domain. Feel free to distribute files of the project on any other website or a platform. Thank you. Peace.

This repository exists to keep the project available after that date. All design credit stays with Denis Aminev. If you redistribute further, keep this attribution intact. See [NOTICE.md](NOTICE.md).

Original joint image gallery: https://timetowaste.ru/joint
