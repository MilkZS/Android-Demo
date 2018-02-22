```
   /**
     * Add content uri in urimatcher
     *
     * @return urimatcher
     */
    public static UriMatcher buildUriMatcher() {
        final UriMatcher matcher = new UriMatcher(UriMatcher.NO_MATCH);
        final String authority = MovieInfoContract.CONTENT_AUTHORITY;
        matcher.addURI(authority, MovieInfoContract.PATH_MOVIE, CODE_MOVIE);
        matcher.addURI(authority, MovieInfoContract.PATH_MOVIE + "/#", CODE_MOVIE_BASE_ID);
        return matcher;
    }
```
