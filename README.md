# d3-tagcloud-for-react ☁️

Another tag cloud for react with two variable fontSize and opacity,
Create beautiful tag/word clouds using React. Uses the wonderful [d3-cloud](https://github.com/jasondavies/d3-cloud) under the hood.



## Installation

	npm install d3-tagcloud-for-react
	or
	yarn add d3-tagcloud-for-react

## Usage

```js
import React, { Component } from 'react'
import SkillsCloud, {renderData} from 'd3-tagcloud-for-react';

const colorarray = [
  '#8c5fc4',
  '#61b8ff',
  '#f7d286',
  '#e86971',
  '#76bb7f',
  '#5bbeca',
]
const data = [
  {
  label: 'React',
  fontSize: 10,
  opacity: 8,
  color:'blue'
  },
  {
  label: 'jQuery',
  fontSize: 9,
  opacity: 9,
  },
  {
  label: 'ECMAScript 6',
  fontSize: 4,
  opacity: 7,
  },
  {
  label: 'webpack',
  fontSize: 4,
  opacity: 4,
  },
  {
  label: 'Redux',
  fontSize: 4,
  opacity: 7,
  },
  {
  label: 'HTML5',
  fontSize: 9,
  opacity: 9,
  },
  {
  label: 'JSON APIs',
  fontSize: 9,
  opacity: 6,
  },
  {
  label: 'JavaScript',
  fontSize: 9,
  opacity: 8,
  },
  {
  label: 'CSS3',
  fontSize: 9,
  opacity: 9,
  },
  {
  label: 'PHP',
  fontSize: 8,
  opacity: 3,
  },
  {
  label: 'MySQL',
  fontSize: 8,
  opacity: 4,
  },
  {
  label: 'WordPress',
  fontSize: 9,
  opacity: 8,
  },
  {
  label: 'Github',
  fontSize: 6,
  opacity: 5,
  },
  {
  label: 'SASS',
  fontSize: 6,
  opacity: 6,
  },
  {
  label: 'Node.js',
  fontSize: 4,
  opacity: 4,
  },
  {
  label: 'JSX',
  fontSize: 8,
  opacity: 5,
  },
  {
  label: 'SEO',
  fontSize: 9,
  opacity: 8,
  },
  {
  label: 'Redux Saga',
  fontSize: 4,
  opacity: 6,
  },
  {
  label: 'Immutable',
  fontSize: 4,
  opacity: 5,
  },
  {
  label: 'CSS Javascript',
  fontSize: 4,
  opacity: 6,
  },
  {
  label: 'GraphQL',
  fontSize: 1,
  opacity: 4,
  },
]

class DemoCloud extends Component {
  render() {
    return (
      <SkillsCloud 
        className='tag-cloud'
        // rotate={() => Math.round(Math.random() * 180)}
        // spiral={1}
        style={{
          fontFamily: 'sans-serif',
          // fontSize: () => Math.round(Math.random() * 50) + 16,
          fontSize: 30,
          // color: () => randomColor(colorArray),
          padding: 5,
          width: '100%',
          height: '600px',
        }}
        data={data}
        colorarray={colorarray}
      >
        {renderData(data)}
        <div 
          style={{
            fontSize: 30,
            fontWeight: 'bold',
            opacity: 0.9,
            padding: 12,
            color: 'black'
          }}
        >
          Black
        </div>

      </SkillsCloud>
    );
  }
}
```

## Documentation

`<SkillsCloud>` props:

name | description | type | default
-----|-------------|------|---------
style.fontSize | Font size needed for calculating layout | Function/Number | `20`
style.fontFamily | Font family needed for calculating layout | Function/String | `serif`
style.fontWeight | Font weight needed for calculating layout | Function/Number | `normal`
style.fontStyle | Font style needed for calculating layout | Function/String | `normal`
style.padding | Padding between tags (px) | Function/Number | `1`
style.color | Color to be used by tags | Function/String | `(none)`
rotate | Rotation in degrees | Function/Number | `0`
spiral | Spiral | Function/String | `archimedean`
random | Randomizer function | Function | `Math.random`

Any component can be used as a child component. `SkillsCloud` scans the child components for the following props for its layout calculation:

name | description | type | default
-----|-------------|------|---------
style.fontSize | Font size needed for calculating layout | Function/Number | `20`
style.fontFamily | Font family needed for calculating layout | Function/String | `serif`
style.fontWeight | Font weight needed for calculating layout | Function/Number | `normal`
style.fontStyle | Font style needed for calculating layout | Function/String | `normal`
style.padding | Padding between tags (px) | Function/Number | `1`
style.color | Color to be used by tag | Function/String | `(none)`
rotate | Rotation in degrees | Function/Number | `0`


## Examples




## Resources

- [https://github.com/jasondavies/d3-cloud](https://github.com/jasondavies/d3-cloud)

## License

[MIT](./LICENSE.txt)