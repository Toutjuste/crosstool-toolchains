Get crosstool-ng :
------------------

Before instalation, make sure you have the required packages instaled.

1. Download crosstool-NG sources: ``wget http://crosstool-ng.org/download/crosstool-ng/crosstool-ng-1.21.0.tar.bz2``
2. Extract them: ``tar -xjvf crosstool-ng-1.21.0.tar.bz2``
3. Run ``cd crosstool-ng-1.21.0``
4. Run ``./configure --prefix=/opt/crosstool-ng-1.21.0``
5. Run ``make`` and ``make install``
6. Add <b>"/opt/crosstool-ng-1.21.0/bin"</b> to your <b>PATH</b> variable

When you want to create a new toolchain (or modify an existing one), run ``ct-ng menuconfig`` in the directory where you want the configuration.

