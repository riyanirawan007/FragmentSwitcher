# FragmentSwitcher
Simple Helper For Switching Between Android Fragments

## Usage
```java
//if you use extra bundle
Bundle bundle=new Bundle();
bundle.putString(ExtraKeys.EXTRA_MOVIE_LIST_STATE,ExtraKeys.MOVIE_LIST_STATE_TOP_RATED);

FragmentSwitcher.getInstance().withContext(context)
                              .withContainer(R.id.home_fragment_container)
                              .withFragmentManager(getActivity().getSupportFragmentManager())
                              .withFragment(new DetailMovieFragment())
                              .withExtraBundle(bundle,null)
                              .setToBackStack(true)
                              .commitReplace();
```
