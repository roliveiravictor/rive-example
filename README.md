# rive-example
Example of how to use Rive with Jetpack Compose

### 1. New Project

- Empty (Compose) Activity with

```
Android Studio Hedgehog | 2023.1.1 Canary 8
Build #AI-231.9011.34.2311.10290408, built on June 9, 2023
Runtime version: 17.0.6+0-17.0.6b829.9-10027231 x86_64
VM: OpenJDK 64-Bit Server VM by JetBrains s.r.o.
macOS 13.4

GC: G1 Young Generation, G1 Old Generation
Memory: 2048M
Cores: 12
Metal Rendering is ON

Registry:
    external.system.auto.import.disabled=true
    debugger.new.tool.window.layout=true
    ide.text.editor.with.preview.show.floating.toolbar=false
    ide.experimental.ui=true

Non-Bundled Plugins:
com.developerphil.adbidea (1.6.11)
```

### 2. Add implementations on the `:app` build gradle

```
implementation("app.rive:rive-android:5.0.0")
implementation("androidx.startup:startup-runtime:1.1.1")
```

### 3. Add the Rive initializer on the Android Manifest

```
<provider
    android:name="androidx.startup.InitializationProvider"
    android:authorities="com.rive.example.androidx-startup"
    android:exported="false"
    tools:node="merge">
    <meta-data android:name="app.rive.runtime.kotlin.RiveInitializer"
    android:value="androidx.startup" />
</provider>
```

### 4. Add the `raw` Resource Folder with a `.riv` file

Riv Files can be browsed [here](https://rive.app/community/).