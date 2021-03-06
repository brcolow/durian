# Durian releases

### Version 3.5.0 - TBD ([javadoc](http://diffplug.github.io/durian/javadoc/snapshot/)) [snapshot](https://oss.sonatype.org/content/repositories/snapshots/com/diffplug/durian/durian/))

### Version 3.4.0 - April 6th ([javadoc](http://diffplug.github.io/durian/javadoc/3.4.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.4.0/view))

* Added `Errors.wrap[Function/Predicate]` methods to handle cases where `Errors.wrap` was ambiguous.
* Added `Either.create(L, R)` for cases where the user knows that exactly one argument will be non-null.
* Added `Either.mapLeft()` and `mapRight()` for transforming `Either`s.
* Improved the performance of the `java.io.Writer` returned by `StringPrinter.toWriter()`.
* Added a `map()` function to `Box.Nullable`. `Box` already had one, its omission from `Box.Nullable` was an oversight.
* Until now, `Errors.rethrow()` wrapped `Error`s inside `RuntimeException`s.  This complicated the stack traces and served no useful purpose.
* Added `TreeQuery.isDescendantOf()` and `isDescendantOfOrEqualTo()`.
* Added `TreeQuery.copyLeavesIn()` and `copyRootOut()`.

### Version 3.3.0 - October 19th ([javadoc](http://diffplug.github.io/durian/javadoc/3.3.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.3.0/view))

* Added `Box.Nullable.modify()`, which has the same behavior as `Box.modify()`.
* OSGi metadata is now auto-generated using bnd.

### Version 3.2.0 - September 14th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/3.2.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.2.0/view))

* Added the `Errors.asTerminal()` method, for treating an `Errors` instance as a `Consumer<Optional<Throwable>>` rather than the usual `Consumer<Throwable>`.
* Added the `TreeQuery.root(TreeDef<T> treeDef, T node)` method, which returns the root node based on the given node.

### Version 3.1.2 - August 19th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/3.1.2/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.1.2/view))

* Fixed a bug in `Throwing.Specific.Bi*` where these interfaces did not throw exceptions - which is the whole reason they exist.

### Version 3.1.1 - July 27th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/3.1.1/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.1.1/view))

* Gah! MANIFEST.MF still had -SNAPSHOT version.  Fixed now.  Would be really nice if we could get MANIFEST.MF generation working.

### Version 3.1 - July 24th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/3.1/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.1/view))

* When `Errors.asRuntime()` wraps an exception as a `RuntimeException`, it now uses `Errors.WrappedAsRuntimeException` rather than a generic `RuntimeException`.

### Version 3.0 - July 19th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/3.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/3.0/view))

* Now available on Maven Central!
* Merged `GetterSetter` and `Box` into just `Box`.
* Rather than `Box` and `Box.NonNull extends Box`, we now have `Box` and `Box.Nullable`.
	+ Non-null by default is much better.
	+ There should not be an inheritance hierarchy between the nullable and non-null versions, and now there isn't.
* Added a mechanism for testing trees for equality.
* Other miscellaneous changes.

### Version 2.0 - May 13th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/2.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/2.0/view))

* Renamed ErrorHandler to Errors.  This was done mainly to avoid name conflicts with the many other ErrorHandler classes that are out in the wild, but it also has the advantage of being shorter.

### Version 1.0.1 - May 13th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/1.0.1/), [jcenter](https://bintray.com/diffplug/opensource/durian/1.0.1/view))

* The Maven POM was missing the FindBugs annotations, which was causing compile warnings for users of the library.  It now includes them under the proper 'provided' scope.

### Version 1.0 - May 13th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/1.0/), [jcenter](https://bintray.com/diffplug/opensource/durian/1.0/view))

* First stable release.

### Version 0.1 - April 20th 2015 ([javadoc](http://diffplug.github.io/durian/javadoc/0.1/), [jcenter](https://bintray.com/diffplug/opensource/durian/0.1/view))

* First release, to test out that we can release to jcenter and whatnot.
