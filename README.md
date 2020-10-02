# hass-setter

Will set states and restore them on start up.

# Setting a State

```
action:
  - service: setter.set
    data:
      entity_id: binary_sensor.test
      state: "on"
      attributes:
        friendly_name: "test"
        device_class: "power"
```

# Deleting a State

```
action:
  - service: setter.delete
    data:
      entity_id: binary_sensor.test
```

# Caution

This will allow you to set ANY state. Even things you shouldn't or things that already exist.

This will allow you to delete ANY state. Even things you shouldn't or things that already exist.

# About

This is, quite literally, the smallest amount of code that will do the job. There are lots of improvements to be made. The majority of the initial code was borrowed from the [saver](https://github.com/PiotrMachowski/Home-Assistant-custom-components-Saver) custom component.

PRs to make this better and do more are requested. 
