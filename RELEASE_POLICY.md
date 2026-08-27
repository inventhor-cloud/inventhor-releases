# Release Policy

A package may be uploaded only after all applicable gates pass:

1. canonical source and version are identified;
2. protected credentials and private data are absent;
3. clean reproducible build passes;
4. focused, regression, install, runtime-smoke, update, and rollback tests pass;
5. release signing identity is verified and is not an Android debug certificate;
6. SHA-256 and signed manifest are generated;
7. compatibility and required permissions are declared;
8. last verified rollback artifact remains available.

Development builds remain in private development storage and must never replace `latest`.

