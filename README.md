# sylb: Incremental syllable boundary detection

The build system is based on CMake. To build, you
should only need to do the following:
```sh
 (edit CMakeLists.txt to suit your environment)
 cmake .
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

To run the decoding, call:
```
  bin/sdec example/example_PLP.mat cfg/PLP_filter.mat
```

[Milos Cernak](http://www.idiap.ch/~mcernak)

June 2015
