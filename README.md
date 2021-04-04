# sm_closestpos
Sourcemod extension to add a type called `ClosestPos` that you create with an ArrayList of positions which can then be queried for the closest index to a given position.

Currently uses an implementation of k-d trees from https://github.com/jlblancoc/nanoflann

Probably going to use this in https://github.com/shavitush/bhoptimer as it will provide much faster "closest replay time" stuff.

Provides the following:
```
methodmap ClosestPos < Handle {
	public native ClosestPos(ArrayList input, int offset=0);
	public native int Find(float pos[3]);
};
```

my building thing
```
cd alliedmodders/sourcemod/public/
git clone git@github.com:rtldg/sm_closestpos.git # https://github.com/rtldg/sm_closestpos.git
cd sm_closestpos
mkdir build
cd build
python3 ../configure.py --enable-optimize --sdks=css,tf2,csgo
ambuild
```
windows
```
# open VS2015 x86 Native Tools Command Prompt
"C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\Common7\Tools\vsdevcmd\ext\vcvars.bat"

cd alliedmodders/sourcemod/public/
git clone git@github.com:rtldg/sm_closestpos.git # https://github.com/rtldg/sm_closestpos.git
cd sm_closestpos
mkdir build
cd build
py ../configure.py --enable-optimize --sdks=css,tf2,csgo
ambuild
```
