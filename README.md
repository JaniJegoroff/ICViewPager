## Motivation

https://groups.google.com/forum/#!msg/calabash-ios/tlsmGHeMPYg/njO3nekpycsJ

This is a sample project to demonstrate UIScrollViewDelegate calls when using Calabash scroll commands

```
scroll('scrollView', :left)
scroll('scrollView', :right)
```

See delegate methods in ViewPagerController.m

```
- (void)scrollViewDidScroll:(UIScrollView *)scrollView
- (void)scrollViewDidEndDecelerating:(UIScrollView *)scrollView
```

## Testing scrollViewDidScroll delegate call

Uncomment below line in scrollViewDidScroll method

```
//[self.view setBackgroundColor:[self randomColor]];
```

Build and launch the app from Calabash console

1. Test scroll behaviour manually
2. Test scroll behaviour using Calabash scroll commands

==> You should see that delegate method gets called in both cases

## Testing scrollViewDidEndDecelerating delegate call

Uncomment below line in scrollViewDidEndDecelerating method

```
//[self.view setBackgroundColor:[self randomColor]];
```

Build and launch the app from Calabash console

1. Test scroll behaviour manually
2. Test scroll behaviour using Calabash scroll commands

==> You should see that delegate method does not get called in case 2