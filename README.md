# evaluate-artifacts-releases

This repository serves as a home for releases of Armory's Evaluate Artifacts plugin for Spinnaker. This plugin is currently in Early Access which means it's pre-1.0 and subject to change. 

## About

Armory's Evaluate Artifacts plugin provides a new stage type, `Evaluate Artifacts`, which allows you to create artifacts for downstream consumption. The generated artifacts will be evaluated for SpEL expressions before being consumed. 

Official documentation for this feature will be added shortly. 

_At the time of this writing, the Evaluate Artifacts plugin is only supported on the 1.24 release of Spinnaker. Support for Armory Spinnaker is forthcoming._

## Installation & Configuration

_It should be noted that the plugins framework for Spinnaker is still in active development so installation instructions may change_.

1. Identify the released version of the Evaluate Artifacts plugin you wish to install. Official releases are found [here](https://github.com/armory-plugins/evaluate-artifacts-releases/releases).
2. In your Spinnaker configuration, add the following repository & plugin configuration.

    ```yaml
    spinnaker:
      extensibility:
          plugins:
              Armory.EvaluateArtifactsPlugin:
                enabled: true
                version: 0.0.13
                extensions:
                  armory.evaluateArtifactsStage:
                    enabled: true
          repositories:
            armory:
              url: https://raw.githubusercontent.com/armory-plugins/evaluate-artifacts-releases/master/repositories.json
    ```
    
3. On startup, the plugin will be downloaded and installed to the appropriate Spinnaker services.


## Feedback

We'd love to hear about how you're using our Evaluate Artifacts plugin! If you have any feedback or questions, just leave us a comment!
