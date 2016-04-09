# FlexGrid
### A Simple Sass grid based on FlexBox
###### In progress

***

Flexgrid can be used in two ways as a scss file relying soley on mixins or as css with presentational class names (coming soon).

## Getting Started - Sass

```sass
// import flexgrid scss
@import 'flexgrid';
```
#### Override FlexGrid defaults

```sass
// Override $fg map with new values
// Defaults -> override only what you need
$fg: (
  width: initial,
  gutter: 10px,
  sm: 480px,
  md: 768px,
  lg: 1024px,
  xlg: 1180px,
);
```

| Option          | What it does             |
| ----------------|:------------------------:|
| width           | Sets max width of row    |
| gutter          | Space between columns    |
| sm, md, lg, xlg | values for break points  |

#### Breakpoints (mobile first)

```sass
// sm, md, lg, xlg
@include breakpoint(md) {
  // styles for medium screens and up
}
@include breakpoint(lg) {
  // styles for large screens and up
}
```

#### Rows

```sass
@include fg-row($horz:start, $vert:start, $wrap:false, $reverse:false);
```
| Option          | Values  | What it does             |
| ----------------|---------|:------------------------:|
| $horz           | start (default), end, center, between, around | Positions the columns horizontal |
| $vert           | start (default), end, center, stretch | Positions the columns vertically |
| $wrap           | false (default), true | Sets flex-wrap |
| $reverse        | false (default), true | Sets flex-direction |


#### Columns

```sass
@include fg-col($size:null, $align:auto, $offset:0, $order:0);
```
| Option          | Values  | What it does             |
| ----------------|---------|:------------------------:|
| $size           | auto (default), 0 -> 1 | Sets column size (default sizes automatically) |
| $align          | start (default, end, center, stretch | Positions this specific column vertically |
| $offset         | 0 (default) -> 1 | Sets margin offset |
| $order          | #                | Sets order of this specific column |



# License

[MIT License.](http://www.opensource.org/licenses/mit-license.php)
