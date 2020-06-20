# [Botzone](https://wiki.botzone.org.cn/index.php?title=%E9%A6%96%E9%A1%B5)
## [Bot](https://wiki.botzone.org.cn/index.php?title=Bot)
### Environment
* Ubuntu 16.04 x86-64, 1 Core
* Programming Language
    * G++ 7.2.0 (-O2, C++17) `.cpp`, `.cc` JSONCPP, nlohmann/json, Eigen
    * G++ 7.2.0 with many lib (-O2, C++17, 带有大量库，详见维基) tensorflow_cc, libtorch, libboost, libopenblas
    * G++ 5.4.0 (-O2, C++11) `.cpp`, `.cc`
    * G++ 5.4.0 (-O2) `.cpp`, `.cc`, `.c`
    * G++ 5.4.0 (-O0) `.cpp`, `.cc`
    * OpenJDK 8 `.java` JSON.simple
    * Node.js 10.0.0 `.js`
    * Python 2.7.12 `.py`
    * Python 3.5.2 `.py`
    * Python 3.6.5 `.py` numpy, scipy, TensorFlow 1.14 (CPU), theano, pytorch 1.4.0, mxnet 0.12.0, keras 2.1.6, lasagne, scikit-image, h5py
    * C# (Mono 5.0.0) `.cs` Newtonsoft.Json
    * Free Pascal 3.0.0 `.pas`

### Resource
* Storage: 128MB `./data`
* Memory: 256MB
* Time: 1sec
    * JavaScript: x2
    * Java: x3
    * C#, Python: x6

### Life Cycle / IO
#### 1-input 1-output
1. Receive *all* interaction, `data` and `globaldata` upon starting
2. Send current action to take as `response`, `data` and `globaldata` to save and `debug` to log
3. exit

#### interactive
1. Receive *first* input, `globaldata` upon starting
2. `while` (receive `request`)
    1. send `response`, `data`, `globaldata` and `debug`
    2. send `">>>BOTZONE_REQUEST_KEEP_RUNNING<<<"`
3. exit

# Detail for 国标麻将
* [Botzone/Chinese-Standard-Mahjong](https://wiki.botzone.org.cn/index.php?title=Chinese-Standard-Mahjong)

# Dataset
## [Officially Provided (PW: rm79)](https://pan.baidu.com/s/1vXzYUsRBNpH245SQku0b3A)
* Reorganized as `{dir}/{year}/{month}/{day}/{id}.txt` for convenience: [`{dir}.zip` = `{dir}/{2017}/{01}`](https://1drv.ms/u/s!AqFAE2dFxukCgrIubIwOJ2cEb3BMCQ?e=0lDJdd)

dir|内容
:--|:--
LIU|流局
MO|摸和
PLAY|点和
