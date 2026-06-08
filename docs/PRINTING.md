# Printing Guide

This document catalogs every printable part, the variations available, recommended orientation, and the dimensional checks you must pass before assembly.

> Source: Infidex 176 V manual by Denis Aminev. Part names match the STL files in `STL/`.

## Print settings (ABS reference profile)

| Setting | Value |
|---|---|
| Nozzle | 0.4 mm |
| Layer height | 0.2 mm |
| First layer height | 0.23 mm (glass bed) |
| Inner perimeters | 4 |
| Min top/bottom thickness | 2 mm |
| Infill | 25% max |
| Bed | 4 mm polished glass, or PEI |

Print order is free, but print the body first to confirm fit. Some small parts benefit from rafts, brims, or mouse ears for first-layer adhesion.

## Dimension checks

Verify after printing the bottom body part. Deviation of 0.2 to 0.4 mm on a printed part is acceptable (not in the slicer, only on the physical part).

| Dimension | Target |
|---|---|
| Body thickness (measured mid-side) | 37.8 mm |
| Model height | 36.03 mm |
| Full body height (unibody) | 67 mm |
| Body length | 168 mm |
| Knob shoulder width | 25.3 mm |
| Inner span | 124 mm |
| Vertical reference | 47.5 mm |
| Rewind knob diameter | ~25 mm |
| Lens barrel reference diameter | ~60 mm |

## Body

Print one of four variants. All use supports in "from bed" mode (tree supports recommended).

| Variant | Files | Notes |
|---|---|---|
| 1 (two-piece) | `BODY_bottom_var1`, `BODY_top_var1` | Standard split body |
| 2 (two-piece) | `BODY_bottom_var2`, `BODY_top_var2` | Adds front M3 brass-insert holes for screwing the helicoid mount |
| 3 (unibody) | `BODY_unibody_var1` | Single piece. "Top to down" orientation may print better (untested) |
| 4 (unibody) | `BODY_unibody_var2` | Single piece with front M3 brass-insert holes |

Two-piece bodies need the seam filled with putty or soldered, and the frame planes kept parallel during gluing (this sets the focus plane).

## Lens mount (choose one)

### Focusing helicoid (recommended)

| Part | Files | Notes |
|---|---|---|
| Mount | `Helicoid_MOUNT_ver1` | Glued to body |
| Mount, screwable | `Helicoid_MOUNT_ver2` | Four holes for M3x10 screws to the body |
| Focus ring | `Helicoid_FOCUS_ring_ribs` | Ribbed grip |
| Focus ring, smooth | `Helicoid_FOCUS_ring_NO_ribs` | Same ring, no ribs |
| Inner ring | `Helicoid_INNER_ring` | Threaded inner barrel |
| Fixation ring | `Helicoid_FIX_ring` | Snaps into the mount groove |
| Lens board | `Helicoid_Lense_BOARD` | Start with this one |
| Lens board, lower | `Helicoid_Lense_BOARD_lower` | Use only if focal length is too long for infinity |

**Blue Dot lens (shorter flange distance):**

| Part | File |
|---|---|
| Inner ring, 2 mm shorter | `Helicoid_INNER_ring_80mm_shorter-2mm` |
| Focus ring, 2 mm shorter | `Helicoid_FOCUS_ring_ribs_shorter-2mm` (or the no-rib equivalent) |

### Classical cone

| Part | Files | Notes |
|---|---|---|
| Cone base | `CONE_lens_classic_BASE` | Also available with M3 holes |
| Lens board | `CONE_lens_classic_BOARD` | |

### Tube mount

| Part | Files |
|---|---|
| Tube mount | `Tube_lens_mount` |
| Lens board | `Tube_Lense_BOARD` |

## Door

Four versions: door with or without film reminder and thumbrest, in different combinations. Print in "from bed" mode with supports. Use rafts or brims if needed.

Orient the door as shown in the manual so it is rigid in both horizontal axes. Printing flat on the door face leaves it too weak to hold closed.

**Note:** the lower ledge sags slightly because of the supports, so remove a little material to fit it into the door frame.

## Small parts

Print these heavy-loaded parts **separately** for strong interlayer adhesion, since combined prints can come out too weak:

- Rewind knob
- Taking spool shaft
- Latch

Other small parts can be printed in one set, and printing them at twice the quantity is sensible because some get damaged during fitting. Small parts that are available in **two variations**: winding knob, rewinding knob, viewfinder.

Functional small parts (exact filenames in `STL/`):

- Spool base
- Taking spool shaft
- Sprockets gear (8-tooth stock) and sprocket shaft
- Frame counter and frame counter cap
- Winding knob (2 variants)
- Rewinding knob (2 variants)
- Latch
- Cold shoe (kit part, or use a third-party shoe)
- Cable release port and lever knob (print at 0.1 to 0.12 mm layer height)
- Viewfinder (2 variants)
- Pressure plate
- Lens hood (2 variants, friction fit, scale to your lens diameter)

## Brass inserts

If you chose a body variant with insert holes:

| Insert | Diameter | Height | Location |
|---|---|---|---|
| M3 | 4.5 mm | 6 mm | Front, for helicoid mount |
| 1/4" | 8 mm | 8 mm | Base, for tripod |

Install with a soldering iron. Remove squeezed-out plastic flush with the body surface afterward.
