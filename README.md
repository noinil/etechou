# ETECHOU (e 手帳)

A LaTeX document package for creating PDF planner (手帳 in Japanese) with date links.  Works well on iPad note-taking softwares.

<img src="/share/screenshot_techou_2022.gif"  width="600">

## Usage

### File structure

- `techou2022.tex`: main TeX file;
- `ctechou.sty`: package file that defines the display styles;
- `tex/*.tex`: segmental TeX files that defines the contents of each subunit.

### Use the ctechou style

Include the package before the main content:
```tex
\usepackage[palette=summer,year=2022]{ctechou}
```
where `palette` is the color palette (four possible values: "spring", "summer", "autumn", and "winter"), and `year` is the year you want to organize.

The commands to create yearly, quarterly, monthly, weekly, and daily calendars are defined in `ctechou.sty`, and can be used as shown in the example file `techou2022.tex`.

Particularly, there are two arguments for the command `\drawweekanddaypage{#1}{#2}`, where #1 and #2 are the first and last day in a year to be included in the PDF, respectively.


### Compilation

```bash
make all
```

### Clean

```bash
make clean
```

### Make changes

As described above, the content of each "block" is defined in the segmental files in the `tex/` directory.  You may want to edit those files to create your own style.


To turn off or change the annoying footer on each page, please comment out the last five to three lines in `ctechou.sty`.
