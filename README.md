# Progress Bar

Xml code



```bash
    <ProgressBar
          android:layout_width="match_parent"
          android:layout_height="5dp"
          android:id="@+id/progress"
          style="?android:attr/progressBarStyleHorizontal"
          android:background="#C8C4C4"
          android:layout_alignParentBottom="true"
          android:progress="20"
          android:visibility="gone">
      </ProgressBar>
```
Java code 

```bash
  //id in progressBar
  ProgressBar progressBar;
  progressBar=(ProgressBar)findViewById(R.id.progress);


  //prosses

    mywebView.setWebChromeClient(new WebChromeClient(){

            @Override
            public void onProgressChanged(WebView view, int newProgress) {

                progressBar.setVisibility(View.VISIBLE);
                progressBar.setProgress(newProgress);
                setTitle("Loading.....");

                if (newProgress ==100){
                    progressBar.setVisibility(View.GONE);
                    setTitle(view.getTitle());

                }

                super.onProgressChanged(view, newProgress);
            }
        });

```


