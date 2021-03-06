# Creating an update site

## From Maven (recommended)

- Install Maven 3.3.9+, make ``mvn`` accessible from path
- Call ``mvn install`` from ``blangDSL/ca.ubc.stat.blang.parent``
- Eclipse site is in ``ca.ubc.stat.blang.repository/target/repository``

**Improved pipeline:** just run ``./update-eclipse-plugin.sh [blang DSL version]`` from ``blangDSL/ca.ubc.stat.blang.parent``, this will take care of publishing to same URL as maven site as well.

## From eclipse

- ``Import projects`` to make sure all sub-projects imported, especially, ``feature`` and ``repository``
- From project ``ca.ubc.stat.blang.repository``, pic ``Export``, then ``Deployable features``.

## Publish

Then, just make the ``repository`` accessible, e.g. by rsync'ing into a subdirectory of ``blang:/usr/share/nginx/blang``, say ``eclipserepo``.