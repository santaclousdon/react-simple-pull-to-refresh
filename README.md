# react-simple-pull-to-refresh

[![npm version](https://badge.fury.io/js/react-simple-pull-to-refresh.svg)](https://badge.fury.io/js/react-simple-pull-to-refresh)
[![license](https://img.shields.io/github/license/thmsgbrt/react-simple-pull-to-refresh.svg)](https://github.com/thmsgbrt/react-simple-pull-to-refresh/blob/master/LICENSE)
![](https://badgen.net/npm/types/react-simple-pull-to-refresh)
![](https://badgen.net/badge/maintained/yes/green)

A Simple Pull-To-Refresh Component for React Application with 0 dependency.
Works for Mobile and Desktop.

## Demo

[Click here 👍](https://thmsgbrt.github.io/react-simple-pull-to-refresh)

## Installation

`npm i react-simple-pull-to-refresh`

## Usage

```jsx
import PullToRefresh from 'react-simple-pull-to-refresh';
```

Pull To Refresh only

```jsx
// ...

return (
  <PullToRefresh onRefresh={handleRefresh}>
    <ul>
      {list.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  </PullToRefresh>
);

// ...
```

Pull To Refresh and Fetch More enabled

```jsx
// ...

return (
  <PullToRefresh onRefresh={handleRefresh} canFetchMore={true} onFetchMore={handleFetchMore}>
    <ul>
      {list.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  </PullToRefresh>
);

// ...
```

## Props Matrix

|        Name         |         Type          | Required |        Default        | Description                                                                 |
| :-----------------: | :-------------------: | :------: | :-------------------: | --------------------------------------------------------------------------- |
|      onRefresh      |       Function        |   true   |                       | Function called when fefresh has been trigerred                             |
|     isPullable      |        boolean        |  false   |         true          | Enable or disable pulling behavior                                          |
|  refreshingContent  | JSX.Element or string |  false   | <RefreshingContent /> | Content displayed when refresh has been trigerred                           |
|   pullingContent    | JSX.Element or string |  false   |  <PullingContent />   | Content displayed when pulling                                              |
|  pullDownThreshold  |        number         |  false   |          67           | Distance to pull in pixel in order to trigger a refresh event               |
| maxPullDownDistance |        number         |  false   |          95           | Maximum distance applied to Children when dragging                          |
|   backgroundColor   |        string         |  false   |                       | Apply a backgroundColor                                                     |
|     onFetchMore     |       Function        |  false   |                       | Enable or disable ability of fetching more                                  |
|    canFetchMore     |        boolean        |  false   |         false         | Enable or disable ability of fetching more                                  |
| fetchMoreThreshold  |        number         |  false   |          100          | Distance from bottom in pixel of the container to trigger a FetchMore event |
|      className      |        string         |  false   |                       |                                                                             |

## Contributing

`npm run dev`

## Changelog

1.1.0: Added a Fetch-More feature
