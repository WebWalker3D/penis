# penis

A tiny Python command-line tool that draws randomized penis ASCII art in your terminal. Each run varies the dimensions and details; use a seed to reproduce a drawing.

## Requirements

Python 3.6 or newer. Uses only the Python standard library—no packages to install.

## Run

```sh
git clone https://github.com/WebWalker3D/penis.git
cd penis
./penis
```

Or run it with `python3 penis`.

## Options

```sh
penis                 # Random drawing
penis --stats         # Drawing with a specimen readout
penis --seed 42       # Reproducible drawing
penis -s 42 --stats   # Reproducible drawing and readout
penis --help          # Show available options
```

When running directly from the checkout, use `./penis` in place of `penis`.

The specimen readout includes length (shaft rows), girth (inner character width), corona flare, circumcision status, veins, drip status, and a random temperament. These are drawing parameters, not physical measurements.

## Install for your user

```sh
mkdir -p ~/.local/bin
install -m 755 penis ~/.local/bin/penis
```

Ensure `~/.local/bin` is on your `PATH`, then run `penis` from any directory.

## How it works

The script builds the drawing from text rows using Python’s `random.Random`. It varies the shaft dimensions, glans and corona, foreskin or scar ring, veins, drips, and scrotum details. `--seed` initializes a repeatable random generator.
