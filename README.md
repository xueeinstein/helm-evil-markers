# helm-evil-markers
[![MELPA](https://melpa.org/packages/helm-evil-markers-badge.svg)](https://melpa.org/#/helm-evil-markers)
[![MELPA Stable](https://stable.melpa.org/packages/helm-evil-markers-badge.svg)](https://stable.melpa.org/#/helm-evil-markers)

Show evil markers list with helm.

## Installation

The package can be installed via [MELPA](https://melpa.org). The package name is **helm-evil-markers**.

## Usage

To enable `helm-evil-markers`, you need to toggle it after Evil initialized. Thus, the configuration in
your `emacs.d` should look like:

```lisp
(require-package 'evil)
(require 'helm-evil-markers)

;; init evil
(evil-mode 1)

;; enable helm-evil-markers
(helm-evil-markers-toggle)
```

Or you can manually enable or disable `helm-evil-markers` by executing `M-x helm-evil-markers-toggle`.

Finally, you can use the Evil keybindings `m-*` and `'-*` to set and get marker. See demo:

![demo](demo.gif)

Note that `helm-evil-markers` supports **evil global markers** (marked with captical letters) to switch
between buffers.

## Customization

If you would like to exclude particular mark letters from selection menu, you may add them to the `helm-evil-markers-exclude-marks`. By default this list will contain `^`, `[`, `]` special marks. Also exclusion is disabled by default, to use exclusion rules, you need to set `helm-evil-markers-exclusion-enabled` to a non-nil value beforehand.
