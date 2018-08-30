# 自定义tablayout子view，控制下划线宽度

```
        tabLayout = findViewById(R.id.tablayout);
        viewpager = findViewById(R.id.viewpager);

        ArrayList<String> strings = new ArrayList<>();
        strings.add("轻轻微微");
        strings.add("轻微轻微");

        ArrayList<Fragment> fragments = new ArrayList<>();
        fragments.add(BaseFragment.newInstance());
        fragments.add(BaseFragment.newInstance());

        tabLayout.addTabs(strings);
        viewpager.setAdapter(new BasePagerAdapter(getSupportFragmentManager(), fragments, strings));
        tabLayout.setupWithViewPager(viewpager);
        viewpager.addOnPageChangeListener(new TabLayout.TabLayoutOnPageChangeListener(tabLayout.getTabLayout()));

```