# Vim

## Replace inside quotes with clipboard

```
vi"p
```

## Open link under cursor

```
gx
```

## Open file under cursor

```
gf
```

## Split navigation

- Swap top/bottom or left/right `Ctrl-w r`

- Break out current window into tab view `Ctrl-w t`

- Close every window in current tabview except the current one `Ctrl-w o`

## Delete all lines in a file

1. navigate to top of file
   `gg`

2. delete all lines
   `dG`

= ggdG

## Copy character under cursor

```
yl
```

## Insert current date

```
:r! date "+\%Y-\%m-\%d"
```

2018-11-03

## Delete all lines containing pattern

```
:g/pattern/d
```

## Insert result of terminal command into vim

```
:r !pwd
:r !date
```
