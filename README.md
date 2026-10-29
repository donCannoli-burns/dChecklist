# dChecklist

> **Original project and credit:** [Prusias-kol/pChecklist](https://github.com/Prusias-kol/pChecklist) by Prusias-kol. This is a separate experimental fork maintained at [donCannoli-burns/dChecklist](https://github.com/donCannoli-burns/dChecklist).
>
> **EXPERIMENTAL — USE AT YOUR OWN RISK.** This fork is not guaranteed to be stable or safe. Review settings and scripts before running them, especially commands that spend turns, change inventory, use the mall, PvP, or ascend. The upstream author is not responsible for modifications in this fork.

Simple KoLmafia script for verifying ownership of items on a checklist.

## Install, update, and remove

Run these commands in the **KoLmafia gCLI** (not your operating system's Git shell).

**Install**
```
git checkout https://github.com/donCannoli-burns/dChecklist main
```

**Update**
```
git update donCannoli-burns-dChecklist-main
```

**Remove this fork**
```
git delete donCannoli-burns-dChecklist-main
```

If you previously installed the original upstream project, use `git list` to confirm its installed project ID before optionally deleting it with `git delete Prusias-kol-pChecklist-main`. Avoid keeping upstream and fork versions installed simultaneously when they supply the same script filenames.

## Dependencies

None declared.

## How to use

The existing script command remains `pChecklist`:

```
pChecklist help
pChecklist crimbo22
```

The first command lists available checklist targets; the second runs the `crimbo22` checklist.

## Known issues

The upstream implementation does not recognize bound familiars and may double-count IOTMs when bound and unbound forms are both present.

## Consolidation status (2026-10-29)

A hardened, read-only implementation now ships with [don_custom_functions](https://github.com/donCannoli-burns/don_custom_functions): `pChecklist.ash`, `don_checklist.ash`, and `don_checklist_lib.ash`, with the public checklist data and upstream MIT notice retained. The original repository remains as historical source. **Back up `personalChecklistData.txt` before uninstalling**; installing the replacement does not overwrite that file. Avoid running both checkouts simultaneously because both ship `pChecklist.ash`.

The absorbed checker validates target/range size, handles list values correctly, includes equipped familiar items via `don_master_lib`, and uses plain text output. This is **experimental and has not yet been compiled in a live KoLmafia client**.
