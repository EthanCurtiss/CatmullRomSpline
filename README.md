# crSpline
[Catmull-Rom splines](https://en.wikipedia.org/wiki/Cubic_Hermite_spline#Catmull%E2%80%93Rom_spline) are a type of [spline](https://en.wikipedia.org/wiki/Spline_(mathematics)) where the input points are also the control points. (to be elaborated on later)

## API
### Constructors
**`crSpline.Spline.new(p0, p1 , p2 , p3 , alpha, tension)`**\
Create a new spline.

**`crSpline.Chain.new(points, alpha, tension)`**\
Create a new chain of splines.

### Spline
A single spline.\
**IMPORTANT: Every method has a "SolveArc___" variant where `alpha` is based on the arc length of the spline.**

**`Spline:SolvePosition(alpha)`**\
Solve position

**`Spline:SolveVelocity(alpha)`**\
Solve velocity

**`Spline:SolveAcceleration(alpha)`**\
Solve acceleration

**`Spline:SolveUnitTangent(alpha)`**\
Solve unit tangent

**`Spline:SolveUnitNormal(alpha)`**\
Solve unit normal

**`Spline:SolveCurvature(alpha)`**\
Solve curvature

**`Spline:SolveCFrame(alpha)`**\
Solve CFrame

**`Spline:SolveLength(a, b)`**\
Solve length from a to b

**`Spline:SolveRotCFrame(alpha)`**\
Solve rotated CFrame
**only for CFrame splines**

### Chains
Multiple splines chained together that act as one spline.\
**Chains have all of the same methods as Splines!**