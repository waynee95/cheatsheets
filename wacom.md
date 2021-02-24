# Wacom

## Map stylus to left half of screen width

```bash
$ xinput set-prop "Wacom Intuos PT M 2 Pen stylus" --type=float "Coordinate Transformation Matrix" 0.5 0 0 0 1 0 0 0 1
```

## Map stylus to right half of screen width

```bash
$ xinput set-prop "Wacom Intuos PT M 2 Pen stylus" --type=float "Coordinate Transformation Matrix" 0.5 0 0.5 0 1 0 0 0 1
```

## Middle mouse buttton scrolling

```bash
$ xsetwacom --set "Wacom Intuos PT M 2 Pen stylus" Button 2 "pan"
```

Increase sensitivity of scrolling:

```bash
$ xsetwacom --set "Wacom Intuos PT M 2 Pen stylus" "PanScrollThreshold" 200

```
