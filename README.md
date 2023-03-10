# react-d3-wrapper

An example of a React component to help use D3 components within a React application in an organised manner. This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Setup 

```
npm install
```

or

```
yarn install
```

## When to use 

In general, you should try to avoid using D3 data binding to modify DOM when developing React apps. Otherwise you'll have two different frameworks, with very different designs and APIs, managing your DOM. Which will make reasoning about the application and debugging more difficult. And likely ends being confusing to many not familiar with both React and D3.

You might DO want D3 to manage DOM within the React applications if:

* you need nice transitions between data updates, especiallly when working with svg paths and polylines and whenever simple CSS transitions/animations won't cut it
* working with axes
* having complex nested data where creating React components might end up more complicated then using D3 nested selection 

You don't need D3 to manage DOM if:

* you want to use it's layout or scale functions or any other utils. These can be used effectively as any other util function within React components where React renders output of theses functions.

## Usage

`

```
import D3Wrapper from "./d3_wrapper";
import D3LineChart from "./d3_line_chart";

<D3Wrapper
  wrapperEl="svg"
  data={data}
  width={width}
  height={height}
  xAxisLabel={"x axis label"}
  yAxisLabels={"y axis label"}
  d3ComponentClass={3LineChart}
/>

```

## License

MIT
