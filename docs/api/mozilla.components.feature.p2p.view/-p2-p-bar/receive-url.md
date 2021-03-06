[android-components](../../index.md) / [mozilla.components.feature.p2p.view](../index.md) / [P2PBar](index.md) / [receiveUrl](./receive-url.md)

# receiveUrl

`fun receiveUrl(neighborId: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, neighborName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`?, url: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html) [(source)](https://github.com/mozilla-mobile/android-components/blob/master/components/feature/p2p/src/main/java/mozilla/components/feature/p2p/view/P2PBar.kt#L105)

Overrides [P2PView.receiveUrl](../-p2-p-view/receive-url.md)

Handles receipt of a URL from the specified neighbor. For example, the view could prompt the
user to accept the URL, upon which [Listener.onSetUrl](../-p2-p-view/-listener/on-set-url.md) would be called. Only an internal
error would cause `neighborName` to be null. To be robust, a view should use
`neighborName ?: neighborId` as the name of the neighbor.

### Parameters

`neighborId` - the endpoint ID of the neighbor

`neighborName` - the name of the neighbor, which will only be null if there was
    an internal error in the connection library

`url` - the URL