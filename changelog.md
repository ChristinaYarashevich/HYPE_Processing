### build_20130521.0 (May 21, 2013)
- new HBehavior method: `registered(boolean)`
- new static HMath method: `round512(float)` (sets rounds a given) float to the nearest 1/152 interval.
- changes to HConstants:
	- new constant: HConstants.Z
	- the values for property constants are have been changed to reflect the inclusion of HConstants.Z
- various HTween refinements and changes:
	- more accurate callback triggering by using `round512()`
	- methods `start()` & `end()` now take ellipsis arguments
	- removed `startPt()`, `endPt()`, `curr()` and `currPt()` and `nextVal()` methods
	- HConstants.Z is now available for HTween
	- z coordinates are now computed with HTween when using HConstants.LOC
	- HTween now passes itself to the callback, instead of the current value

### build_20130520.0 (May 20, 2013)
- bugfix: `HColorPool.getColor(int)` didn't properly seed their colors
- renamed `HDrawable._alpha` into `_alphaPerc`
- initial documentation contents for HDrawable
- width and/or height in `HDrawable.anchor(float,float)`, `anchorX(float)` and `anchorY(float)` are now assumed to be 100 when its width and/or height is 0 to prevent division-by-zero errors.
- new method: `HSwarm.addGoal(float,float,float)`

### build_20130517.0 (May 17, 2013)
- new file: changelog.txt
- migrate documentation from markdown to Doxygen
- set the default size of HDrawable from 64x64 to 100x100
- the values for HConstants.DEFAULT\_WIDTH & DEFAULT\_HEIGHT are now 100
- new HMouse method: `moved()`
- rename: HColorUtil -> HColors
- remove deprecated HColors methods:
	- `multiply()`
	- `multiplyAlpha()`
	- `multiplyRed()`
	- `multiplyGreen()`
	- `multiplyBlue()`
- migrate PApplet math calls to Math
- various new HMath methods:
	- `dist()`
	- `random()`
	- `map()`
- remove deprecated `HMath.init()` method
- remove unimplemented HEventTrigger
- new HDrawable methods:
	- `firstChild()`
	- `lastChild()`
- HVector is _no longer_ a subclass of PVector. Now it's just a container of x, y & z values