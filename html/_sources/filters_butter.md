---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.13.8
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

```{code-cell} ipython3
:tags: [remove-cell]
%matplotlib inline
```

# Removing frequencies using a Butterworth filter

The Butterworth filter may be the most used filter in biomechanics. It targets ranges of frequencies to remove from the signal's frequency spectrum. A classic use is to estimate the frequency range of both the data and noise, then use the filter to keep most of the data's frequency range while filtering out most of the noise's frequency range. In this tutorial, we will see how to apply Butterworth filters on TimeSeries data, using the [filters.butter()](api/kineticstoolkit.filters.butter.rst) function.

```{code-cell} ipython3
import kineticstoolkit.lab as ktk
import matplotlib.pyplot as plt
```

We begin by loading some sample data:

```{code-cell} ipython3
ts_noisy = ktk.load(ktk.doc.download("filters_noisy_signals.ktk.zip"))

ts_noisy.plot()
plt.title("Noisy signals")
plt.tight_layout()
```

## Low-pass no-lag filter

Here is an example of how to filter out high frequencies using a no-lag Butterworth filter of order 2:

```{code-cell} ipython3
plt.subplot(1, 3, 1)
ts_noisy.plot()
plt.title("Before filtering")

plt.subplot(1, 3, 2)
temp = ktk.filters.butter(ts_noisy, fc=20)
temp.plot()
plt.title("Low-pass 2nd order at 20 Hz")
plt.tight_layout()

plt.subplot(1, 3, 3)
temp = ktk.filters.butter(ts_noisy, fc=4)
temp.plot()
plt.title("Low-pass 2nd order at 4 Hz")
plt.tight_layout()
```

As expected, when filtering lower frequencies, the signal is clearer but transitions are less sharp and some very dynamic information may be lost.

## High-pass no-lag filter

Here is an example of how to filter out low frequencies using a no-lag Butterworth filter of order 2.

```{code-cell} ipython3
plt.subplot(1, 2, 1)
ts_noisy.plot()
plt.title("Before filtering")

plt.subplot(1, 2, 2)
temp = ktk.filters.butter(ts_noisy, btype="highpass", fc=60)
temp.plot()
plt.title("High-pass 2nd order at 60 Hz")
plt.tight_layout()
```

As expected, only the transitions are kept; all the stable parts of the signal were removed.
