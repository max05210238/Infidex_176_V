# Handoff for Claude Code

This file tells you (Claude Code, running in the user's local environment) what
this bundle is and exactly what to do. The user wants you to commit and push
everything to their GitHub repo. You have their git credentials locally; the
chat-side assistant did not, which is why this work is being handed to you.

## Repository

- URL: https://github.com/max05210238/Infidex_176_V
- Default branch: `main`
- Current state: empty (this will be the initial commit)

## Context: what this repo is

A community **preservation mirror** of the open source **Infidex 176 V** 3D
printed panoramic 35mm film camera, designed by **Denis Aminev** (Time to Waste).
The author's original site (timetowaste.ru) goes offline on 21 March 2027 and he
explicitly permitted redistribution on any platform:

> Feel free to distribute files of the project on any other website or a platform.

All design credit stays with Denis Aminev. Keep `NOTICE.md` intact in any commit.

## What was produced (in this bundle)

Reorganized English documentation built from the author's PDF manual and build
video, plus an LFS config:

```
README.md                      Project overview, specs, BOM, print settings, file tree, credits, license note
NOTICE.md                      Attribution + redistribution permission (keep intact)
.gitattributes                 Git LFS rules for .max/.stl/.fbx/.3mf/.obj/.zip
HANDOFF.md                     This file (can be deleted before/after committing, optional)
docs/PRINTING.md               Part catalog (all STL names), print settings, dimensions, brass inserts
docs/ASSEMBLY.md               14-step build
docs/FOCUSING_AND_USAGE.md     Focus calibration, Mamiya 80mm DOF table, shooting, scanning
docs/VIDEO_TRANSCRIPT.md       Chaptered build-video transcript
STL/README.md  FBX/README.md  MODS/README.md   Folder description stubs
```

The original `Infidex 176 V manual.pdf` was NOT modified. It should be committed
unchanged as the source-of-truth manual.

## What the user still needs to add (binary files, NOT in this bundle)

The user has these locally and will drop them into the repo working tree:

```
Infidex 176 V manual.pdf       -> repo root
Infidex 176 V_NEWEST.max       -> repo root  (3ds Max master CAD)
STL/   real .stl files
FBX/   real .fbx files
MODS/  community mod files
```

## Tasks for you (Claude Code)

1. Confirm the repo is cloned and the working tree contains BOTH this bundle's
   files AND the user's binary files (.pdf, .max, STL/, FBX/, MODS/). If the
   binaries are missing, ask the user where they are before committing.

2. Ensure Git LFS is set up (needed because .max and STL/FBX can exceed GitHub's
   100 MB per-file hard limit):
   ```
   git lfs install
   ```
   `.gitattributes` is already provided and tracks .max/.stl/.fbx/.3mf/.obj/.zip.

3. Sanity check before committing:
   - File/folder names match what the docs reference (part names in docs/PRINTING.md).
   - No accidental secrets, no slicer temp junk. Add a .gitignore if you see any.
   - Verify large files are staged through LFS: `git lfs status` should list the
     .max and .stl files.

4. Commit and push to `main`:
   ```
   git add .gitattributes
   git add .
   git commit -m "Initial mirror: Infidex 176 V (docs + source files)"
   git push -u origin main
   ```

5. After push, report back: confirm LFS objects uploaded, and flag anything that
   hit a size or LFS-quota issue.

## Caveats to mention to the user

- GitHub Free Git LFS quota is limited (about 1 GB storage and 1 GB/month
  bandwidth by default). If the STL set plus the .max blow past that, an
  alternative is to commit the docs + manual normally and attach the heavy
  binaries (a zipped STL pack, the .max) to a GitHub **Release** instead of LFS.
- The chat-side assistant could not push directly (separate ephemeral sandbox,
  no access to the user's credentials, and it does not enter tokens/credentials
  into fields). That is expected. You are the right place to do the push.

## Conversation summary (what we discussed)

1. User shared the Infidex 176 V PDF manual + a build-video transcript and a
   screenshot of their local file tree (FBX/, manual.pdf, .max, MODS/, STL/).
2. Goal: fully document/preserve the open-source project into the user's new
   (empty) GitHub repo so other enthusiasts can keep using it after the original
   site shuts down in March 2027.
3. Chat-side assistant read the whole project and produced the English docs in
   this bundle, matching the planned repo structure and keeping original part
   names and full attribution.
4. Assistant could not push (no local credentials in its sandbox). Plan: hand
   the bundle to Claude Code, which has the user's local git auth, to commit and
   push to `main`. Git LFS suggested for the large .max/STL files.
