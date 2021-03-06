# Find service area interactive

This sample demonstrates how to find services areas around a point. A service area shows locations that can be reached from a facility based off a certain impedance [such as travel time]. Barriers can also be added which can affect the impedance by not letting traffic through or adding the time is takes to pass that barrier.

## How to use the sample

Use the segmented control in the toolbar to switch between `Facilities` and `Barriers`. To add a facility click on a location on map and a marker will be added. For barrier, click on the map to draw buffered polygon. You can use the sliders to change the time breaks. Then click the `Service Area` button to get the service area for added facilities. Click on the clear button (trash) to start over.

![](image1.png)

## How it works

The sample uses the `defaultServiceAreaParameters(completion:)` method on `AGSServiceAreaTask` to get the default parameters from the service. Barriers are created using the initializer `init(polygon:)` on `AGSPolygonBarrier`. Sets the facilities and barriers in the parameters. Then uses the `solveServiceArea(with:completion:)` method to solve for the route. Once the result is in, the sample displays the service areas for individual facilities using `resultPolygons(atFacilityIndex:)` method on `AGSServiceAreaResult`.






