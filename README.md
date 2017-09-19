# feta
Feta is Axios' CSS styleguide. Sprinkle it on your project for maximum flavor.

## Variables

Variables cam be edited in `src/variables`

### Typography

```scss
// FONTS
$sans: "Gordita", Helvetica, Arial, sans-serif !default;
$serif: "Atiza", Georgia, serif !default;
$mono: "Liberation Mono", monospace !default;

// TYPOGRAPHY
$base-font-size: 16px !default;
$regular: 400 !default;

// SPACING
$space-05: .25rem !default; // 4px
$space-1: .5rem   !default; // 8px
$space-2:   1rem  !default; // 16px
$space-3: 1.5rem  !default; // 24px
$space-4:   2rem  !default; // 32px
$space-5:   3rem  !default; // 48px
$space-6: 4.5rem  !default; // 72px
```

### Colors

```scss
$color-map: (
  axios-blue: (
    100: #96d8ff,
    200: #75cdf9,
    300: #3faff3,
    400: #069cda,
    500: #008dc8,
    600: #027bb9,
    700: #0064a3,
    800: #004e89,
    900: #01356e,
  ),
  tomato: (
    100: #ffd1c6,
    200: #ffb3a0,
    300: #fb937a,
    400: #f97353,
    500: #e74e29,
    600: #d9421e,
    700: #ca330f,
    800: #ba2f0e,
    900: #b1290a,
  ),
  orange: (
    100: #ffd7b2,
    200: #ffd0a1,
    300: #ffb87e,
    400: #ff9b5a,
    500: #ff7921,
    600: #ff6602,
    700: #f35d00,
    800: #e15300,
    900: #d44b00,
  ),
  purple: (
    100: #d1cdff,
    200: #b7b0ff,
    300: #9686f7,
    400: #7d61e1,
    500: #6741d4,
    600: #602fca,
    700: #551bb7,
    800: #4713a2,
    900: #3d0e87,
  ),
  khaki: (
    100: #ebe2d7,
    200: #dbcfc1,
    300: #d3c3af,
    400: #c1af9a,
    500: #b09d86,
    600: #a8947b,
    700: #a18c72,
    800: #947f65,
    900: #846f55,
  ),
  gray: (
    100: #f5f5f5,
    200: #dcdcdc,
    300: #c2c2c2,
    400: #a9a9a9,
    500: #979797,
    600: #858585,
    700: #696969,
    800: #4a4a4a,
    900: #222222,
  ),
  green: (
    100: #74ffb9,
    200: #46f5ad,
    300: #03e59f,
    400: #00d38f,
    500: #03c183,
    600: #00ac79,
    700: #009a68,
    800: #00865b,
    900: #01724c
  ),
);

// Writing map-get(map-get(...)) is annoying so this utility function compresses it into a single
// command.
@function color-get($color, $saturation: 500) {
  @return map-get(map-get($color-map, $color), $saturation)
}

// Axios Blue Tones
$color-axios-blue-100: color-get(axios-blue, 100);
$color-axios-blue-200: color-get(axios-blue, 200);
$color-axios-blue-300: color-get(axios-blue, 300);
$color-axios-blue-400: color-get(axios-blue, 400);
$color-axios-blue-500: color-get(axios-blue, 500);
$color-axios-blue-600: color-get(axios-blue, 600);
$color-axios-blue-700: color-get(axios-blue, 700);
$color-axios-blue-800: color-get(axios-blue, 800);
$color-axios-blue-900: color-get(axios-blue, 900);
$color-axios-blue: $color-axios-blue-500;

// Tomato Tones
$color-tomato-100: color-get(tomato, 100);
$color-tomato-200: color-get(tomato, 200);
$color-tomato-300: color-get(tomato, 300);
$color-tomato-400: color-get(tomato, 400);
$color-tomato-500: color-get(tomato, 500);
$color-tomato-600: color-get(tomato, 600);
$color-tomato-700: color-get(tomato, 700);
$color-tomato-800: color-get(tomato, 800);
$color-tomato-900: color-get(tomato, 900);
$color-tomato: $color-tomato-500;

// Orange Tones
$color-orange-100: color-get(orange, 100);
$color-orange-200: color-get(orange, 200);
$color-orange-300: color-get(orange, 300);
$color-orange-400: color-get(orange, 400);
$color-orange-500: color-get(orange, 500);
$color-orange-600: color-get(orange, 600);
$color-orange-700: color-get(orange, 700);
$color-orange-800: color-get(orange, 800);
$color-orange-900: color-get(orange, 900);
$color-orange: $color-orange-500;

// Purple Tones
$color-purple-100: color-get(purple, 100);
$color-purple-200: color-get(purple, 200);
$color-purple-300: color-get(purple, 300);
$color-purple-400: color-get(purple, 400);
$color-purple-500: color-get(purple, 500);
$color-purple-600: color-get(purple, 600);
$color-purple-700: color-get(purple, 700);
$color-purple-800: color-get(purple, 800);
$color-purple-900: color-get(purple, 900);
$color-purple: $color-purple-500;

// Khaki Tones
$color-khaki-100: color-get(khaki, 100);
$color-khaki-200: color-get(khaki, 200);
$color-khaki-300: color-get(khaki, 300);
$color-khaki-400: color-get(khaki, 400);
$color-khaki-500: color-get(khaki, 500);
$color-khaki-600: color-get(khaki, 600);
$color-khaki-700: color-get(khaki, 700);
$color-khaki-800: color-get(khaki, 800);
$color-khaki-900: color-get(khaki, 900);
$color-khaki: $color-khaki-500;

// Gray Tones
$color-gray-100: color-get(gray, 100);
$color-gray-200: color-get(gray, 200);
$color-gray-300: color-get(gray, 300);
$color-gray-400: color-get(gray, 400);
$color-gray-500: color-get(gray, 500);
$color-gray-600: color-get(gray, 600);
$color-gray-700: color-get(gray, 700);
$color-gray-800: color-get(gray, 800);
$color-gray-900: color-get(gray, 900);
$color-gray: $color-gray-500;

// Green Tones
$color-green-100: color-get(green, 100);
$color-green-200: color-get(green, 200);
$color-green-300: color-get(green, 300);
$color-green-400: color-get(green, 400);
$color-green-500: color-get(green, 500);
$color-green-600: color-get(green, 600);
$color-green-700: color-get(green, 700);
$color-green-800: color-get(green, 800);
$color-green-900: color-get(green, 900);
$color-green: $color-green-500;

// Primary Colors
$color-axios-black: $color-gray-900;

// UI grays
$color-body-text: $color-gray-800;
$color-site-background: $color-gray-100;
```

## Mixins

### prefix

Example:

```scss
p {@include prefix((transform: translate(-50%, -50%)), webkit ms);}
```
