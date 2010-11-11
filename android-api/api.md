!SLIDE

# Android API #

!SLIDE bullets

* Activity
* View
* BroadcastReceiver
* Service
* XML config

!SLIDE
# Callbacks #

!SLIDE

    public void Activity.onCreate(Bundle bundle)
    public void Activity.onPause()
    public void onClick(View view)


!SLIDE

    @@@ruby
    handle_create do |bundle|
    handle_pause do
    handle_click do |view|

!SLIDE

# HOW? #

!SLIDE bullets

# Java API #

* YourActivity < Activity
* You implement callback methods

!SLIDE bullets

# Ruboto #

* YourActivity < RubotoActivity < Activity
* RubotoActivity implements callbacks
* They tell Ruby to exec blocks, pass params along
