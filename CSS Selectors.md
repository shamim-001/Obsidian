#css #selectors

```css
%% Combining selectors %%
span, li 

%% sibling selectors %%
ul > li



%% Every single li that comes after li with a class of red %%
li.red ~ li

%% Only the very next li that comes after li with a class of red %%
li.red + li



%% Every single li that we hover over %%
li:hover

%% when we click on the input %%
input:focus

%% which input has required %%
input:required

%% input which has type="checkbox" and it is checked %%
input:checked

%% when it has disabled %%
input:disabled


%% it only selects the very first child %%
li:first-child

%% it only selects the very last child %%
li:last-child

%% if it is the only child %%
li:only-child


li:nth-child(3)
```


