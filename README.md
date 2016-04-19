# My Applet

Minimal working *unsigned* applet example.

## Requirements

The site's URL where the applet will get deployed needs to be whitelisted in the
Java control panel. Go to *Java Control Panel > Security > Edit Site List* and add
`http://localhost:8000`.

It's also useful to enable the Java console and logging. Go to *Java Control Panel > Advanced* and tick *Enabled logging* and select
*Show console*.

After this when an applet starts a Java console will also start. Printing
something to `System.out` will end up here.

## Running

Execute `./gradlew run`, which will build the project, copy `my-applet.jar` and
`index.html` under `build/install/my-applet` and serve that directory via HTTP
using `python -m SimpleHTTPServer`.

After this open `http://localhost:8000` to see the applet in action or run
`appletviewer http://localhost:8000`. When the applet loads it should print
`Hello World!` to the console.
