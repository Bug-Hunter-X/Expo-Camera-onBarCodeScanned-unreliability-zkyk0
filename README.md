# Expo Camera onBarCodeScanned unreliability

This repository demonstrates a bug in Expo's Camera API where the `onBarCodeScanned` callback function is not always reliable.  The function may fail to fire, or experience significant delays, seemingly at random. This makes implementing reliable barcode scanning with Expo challenging.

The `bug.js` file contains a simple barcode scanner app showcasing this unreliability. The `bugSolution.js` demonstrates a potential workaround, though not a complete fix. 

## Reproduction
1. Clone this repository.
2. Run `npm install`.
3. Run `expo start`.
4. Point the camera at a barcode. Note the inconsistent timing of barcode recognition, or lack thereof.

## Potential Workarounds (See bugSolution.js)
While there isn't a definitive fix,  some strategies may improve consistency:
* Reduce scanning frequency: Limit how often the camera checks for barcodes.
* Employ a timer:  If a barcode isn't detected after a period, trigger another scan.
* Consider alternative libraries: Explore other barcode scanning libraries for React Native.

This issue is likely related to underlying performance issues or limitations in the Expo Camera implementation.  Contributing to the issue and offering alternative solutions are welcome.