### Single slider

Similar to `<input type="range" defaultValue={50} />`

```jsx
initialState = { value: 0 };

<ReactSlider
    className="horizontal-slider"
    value={state.value}
    onChange={value => setState({ value })}
    orientation="horizontal"
    ariaLabel="This is a single handle"
>
    <div>{state.value}</div>
</ReactSlider>
```

### Double slider (with bars between the handles)

```jsx
initialState = { value: [0, 100] };

<ReactSlider
    className="horizontal-slider"
    value={state.value}
    onChange={value => setState({ value })}
    orientation="horizontal"
    withBars
    ariaLabel={['Lower handle', 'Upper handle']}
    ariaValuetext="Some arbitrary value"
    pearling
    minDistance={10}
>
    {state.value.map((value, i) => <div key={i}>{value}</div>)}
</ReactSlider>
```

### Multi slider

```jsx
initialState = { value: [0, 50, 100] };

<ReactSlider
    className="horizontal-slider"
    value={state.value}
    onChange={value => setState({ value })}
    orientation="horizontal"
    withBars
    ariaLabel={['Leftmost handle', 'Middle handle', 'Rightmost handle']}
    pearling
    minDistance={10}
>
    {state.value.map((value, i) => <div key={i}>{value}</div>)}
</ReactSlider>
```

### Vertical slider

```jsx
initialState = { value: [0, 50, 100] };

<ReactSlider
    className="vertical-slider"
    value={state.value}
    onChange={value => setState({ value })}
    orientation="vertical"
    withBars
    invert
    ariaLabel={['Lowest handle', 'Middle handle', 'Top handle']}
    pearling
    minDistance={10}
>
    {state.value.map((value, i) => <div key={i}>{value}</div>)}
</ReactSlider>
```