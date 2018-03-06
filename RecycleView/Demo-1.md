```
@Override
public MyPicRecycleHolder onCreateViewHolder(ViewGroup parent, int viewType) {
    context = parent.getContext();
    int layoutList = R.layout.fragment_card_food_recipe;
    LayoutInflater inflater = LayoutInflater.from(context);
    View view = inflater.inflate(layoutList,parent,false);
    return new MyPicRecycleHolder(view);
}
```
