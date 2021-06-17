# 通信工学（変調）

Communication Engineering (Modulation)

## 目的 Objective

AM・FM変調方式について数値解析を行い、周波数特性を理解する。

Analyze amplitude and frequency modulation system and understand their frequency characteristics.

## 理論 The basics

次の言葉を含むよう、各自調べてまとめること。箇条書きでなく、文章で記述すること。

Research and summarize a theory to include the following words.

- フーリエ変換 Fourier transform
- 振幅変調 Amplitude modulation
- 周波数変調 Frequency modulation
- 過変調 Overmodulation

## 実験方法 Experiment method

以下の実験を任意のプログラミング言語で行うこと。

Do the following experiments in a programming language of your choice.

参考としてPythonプログラムを提供する。

A Python program is provided for reference.

[github.com/ohashi-gnct/exp4e/blob/master/communication/communicationeng.ipynb](https://github.com/ohashi-gnct/exp4e/blob/master/communication/communicationeng.ipynb)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ohashi-gnct/exp4e/blob/master/communication/communicationeng.ipynb)


### 時間波形とフーリエ変換 Fourier transformation of waveform

cos波 $ f(t)=\cos{(2\pi t/T)} (0<t\leqq T) $ を離散化し、フーリエ変換する。

We discretize the cosine wave $ f(t)=\cos{(2\pi t/T)} (0<t\leqq T) $ and Fourier transform it.

時間刻みを $ \Delta t $ とし、$ N=T/\Delta t $ とすることで、

$ t=i\Delta t (1\leqq i \leqq N) $ と時間を離散化できる。

By setting the time increments as $ \Delta t $ and $ N=T/\Delta t $ ,

we can discretize the time as $ t=i\Delta t (1\leqq i \leqq N) $

これによってcos波を離散化すると、$ f(i\Delta t)=\cos{(2\pi i/N)} $ となる。

Discretizing the cosine wave, we get $ f(i\Delta t)=\cos{(2\pi i/N)} $ .

離散化したcos波について、離散フーリエ変換を行い結果を図示せよ。

For a discretized cosine wave, perform a discrete Fourier transform and show the result.

### 振幅変調 Amplitude modulation

上のcos波をAM変調すると、以下の式となる。

Amplitude modulation of the cosine wave above is the following equation.

$$ V_{AM}(i\Delta t)=\left(1+m_a \cos{(2\pi i f_s /N)}\right)\cos{(2\pi f_c i/N)} $$

振幅変調した波形について、フーリエ変換を行い結果を図示せよ。

Perform a Fourier transform on the amplitude-modulated waveform and show the results.

ただし、$ f_c=10, N=256, i=(1, 2, 3, \ldots , 256) $とする。

The values for each parameters are as follows:

$ f_c=10, N=256, i=(1, 2, 3, \ldots , 256) $

その他のパラメータは適切に変更し、変化を確認する。

Other parameters should be changed as appropriate and changes should be checked.

### 周波数変調 Frequency modulation

上のcos波を周波数変調すると、以下の式となる。

Frequency modulation of the cosine wave above is the following equation.

$$ V_{FM}(i\Delta t)=\cos{(2\pi i f_c/N+\beta \sin{(2\pi i f_s/N)})} $$

周波数変調した波形について、フーリエ変換を行い結果を図示せよ。

Perform a Fourier transform on the frequency-modulated waveform and show the results.

ただし、$ f_c=10, N=256, i=(1, 2, 3, \ldots , 256) $ とする。

The values for each parameters are as follows:

$ f_c=10, N=256, i=(1, 2, 3, \ldots , 256) $

その他のパラメータは適切に変更し、変化を確認する。

Other parameters should be changed as appropriate and changes should be checked.

## 検討課題 Discussion

(1) アナログ変調とディジタル変調の違いを説明せよ。

Explain the difference between analog modulation and digital modulation.

(2) 5G（第5世代移動通信システム）で使われている変調方式を説明せよ。

Explain the modulation system used in 5G (5th generation mobile communication system).

