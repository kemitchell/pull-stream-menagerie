# A pull-stream Menagerie

A breathtaking collection of delectable everyday functions of great help in [pull-stream] journeys.

[pull-stream]: https://www.npmjs.com/package/pull-stream

## Sources

- ... of `Number`, counting from `0` to some `max`

  ```javascript
  require('pull-stream').count(max)
  ```

- with no data

  ```javascript
  require('pull-stream').empty()
  ```

- from a single value

  ```javascript
  require('pull-stream').once(value, onAbort)
  ```

- immediately aborting with an error

  ```javascript
  require('pull-stream').error(error)
  ```

- a synchronous function that returns an infinite number of values

  ```javascript
  require('pull-stream').infinite(generator)
  ```

- an `Array`

  ```javascript
  require('pull-stream').values(array)
  ```

- an `Object`

  ```javascript
  require('pull-stream').values(object) // streams values
  ```

## Sinks

- to `Array`

  ```javascript
  require('pull-stream').collect(function (error, array) { })
  ```

- to `String`

  ```javascript
  require('pull-stream').concat(function (error, string) { })
  ```

- to a synchronous `function (data) { }`

  ```javascript
  require('pull-stream').drain(
    function write (data) { },
    function onEnd (error) { }
  )
  ```

- to a single value matching a synchronous predicate

  ```javascript
  require('pull-stream').find(
    function predicate (data) { },
    function onEnd (error) { }
  )
  ```

- to `console.log`

  ```javascript
  require('pull-stream').log()
  ```

- to nowhere, with a callback on end

  ```javascript
  require('pull-stream').onEnd(function (error) { })
  ```

- to a synchronous reduction function

  ```javascript
  require('pull-stream').reduce(
    function reduction (previousValue, currentValue) {
      return nextValue
    },
    initialValue,
    function onEnd (error) { }
  )
  ```

## Throughs

## Duplexes

## Node Streams

## Node Streams
