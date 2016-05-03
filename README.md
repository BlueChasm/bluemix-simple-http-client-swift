#SimpleHttpClient

[![Swift][swift-badge]][swift-url]
[![Platform][platform-badge]][platform-url]

[swift-badge]: https://img.shields.io/badge/Swift-3.0-orange.svg
[swift-url]: https://swift.org
[platform-badge]: https://img.shields.io/badge/Platforms-OS%20X%20--%20Linux-lightgray.svg
[platform-url]: https://swift.org

## Installation
```swift
import PackageDescription

let package = Package(
    dependencies: [
        .Package(url: "https://github.com/ibm-bluemix-mobile-services/bluemix-simple-http-client-swift.git", majorVersion: 0, minor: 1)
    ]
)

0.1.x releases of SimpleHttpClient are tested on OSX and Linux with DEVELOPMENT-SNAPSHOT-2016-04-25-a


```
## Setup

The SimpleHttpClient is a simple abstraction layer on top of https://github.com/IBM-Swift/Kitura-net

#### Build on Linux

```bash
sudo apt-get update
swift build -Xcc -fblocks -Xlinker -ldispatch
```

### Build on Mac:

```bash
swift build
```

## Using on Bluemix

TBD

## Usage

```swift
let httpResource = HttpResourse(schema: "http", host: "httpbin.org", port: "80")
let headers = ["Content-Type":"application/json"];
let data = NSData()

let resource = httpsResource.resourceByAddingPathComponent(pathComponent: "/post")
HttpClient.post(resource: resource, headers: headers, data: data) { error, status, headers, data in
	if let error = error{
		print("Failure")
	else {
		print("Success")
	}
}
```

## License

This project is released under the Apache-2.0 license

[swift-badge]: https://img.shields.io/badge/Swift-3.0-orange.svg
[swift-url]: https://swift.org
[platform-badge]: https://img.shields.io/badge/Platforms-OS%20X%20--%20Linux-lightgray.svg
[platform-url]: https://swift.org
