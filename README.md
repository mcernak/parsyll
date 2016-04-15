# parsyll: Speech Syllable Parser

The build system is based on CMake. To build, you
should only need to do the following:
```sh
 (edit CMakeLists.txt to suit your environment)
 cmake .
 (or for a debug build call:)
 cmake -D CMAKE_CXX_FLAGS_DEBUG:STRING="-g -Wall -Werror" -D CMAKE_BUILD_TYPE=debug .
 make
```

The technical aspects of the sylb detector are written up in this paper:
```
@InProceedings{Hyafil2015,
  author =       "Hyafil, Alexandre and Cernak, Milos",
  title =        "Neuromorphic Based Oscillatory Device for Incremental Syllable Boundary Detection",
  booktitle =    "Proceedings of Interspeech",
  year =         2015,
  address =      "Dresden, German",
  month =        "September"
}
```
and here is a [pdf](http://publications.idiap.ch/downloads/papers/2015/Hyafil_INTERSPEECH_2015.pdf).

To run the decoding from a htk input PLP feature file, call:
```
  HCopy -C cfg/PLP_0.cfg example/timit_train_dr3_madc0_sa1.wav example/example_PLP.htk
  bin/nsylb -i example/example_PLP.htk	
```

To run the decoding from some matlab input PLP feature file, call:
```
  bin/nsylb -m -n 10 -i example/example_PLP.mat
```

Alternatively, run the shell script (the scrit includes DLOP pitch parametrisation):
```
  run.sh example/timit_train_dr3_madc0_sa1.wav
```

Please note that the nsylb is a stochastic decoder, i.e., it always gives slightly different results for the same input file. In addition, the current version does not include a voice activity detection, i.e., it outputs putative syllable boundaries also for speech silence.
 

[Milos Cernak](http://www.idiap.ch/~mcernak)

July 2015
