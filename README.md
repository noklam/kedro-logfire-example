# kedro-logfire-example

[![Powered by Kedro](https://img.shields.io/badge/powered_by-kedro-ffc900?logo=kedro)](https://kedro.org)


# Update the logging.yml
`logfire` provide a `LogfireLoggingHandler` which already log messages to console. So you can disable the default `rich` style console handler and registed `LogfireLoggingHandler` as follow:

```diff
handlers:
  ...
+  logfire:
+    class: logfire.LogfireLoggingHandler

-  rich:
-    class: kedro.logging.RichHandler
-    rich_tracebacks: True
-    # Advance options for customisation.
-    # See https://docs.kedro.org/en/stable/logging/logging.html#project-side-logging-configuration
-    # tracebacks_show_locals: False

```