!SLIDE
# Demo #

!SLIDE bullets
# Prerequisites #

* Java
* JRuby (rvm)
* Android SDK
* Generate an emulator
* gem install ruboto-core

!SLIDE bullets
# Generate App #

    $ ruboto gen app \
    $ --package com.danieljackoway.rubyconfx \
    $ --path rubyconfx \    # where app files go
    $ --name HelloWorld \   # Name of app
    $ --target android-8 \  # Froyo
    $ --activity HiActivity # Name of Activity

(remove comments)

* Basically same args as `android create project`

!SLIDE
# assets/scripts/hi_activity.rb

    @@@ruby
	require 'ruboto.rb'

	ruboto_import_widgets :TextView,
      :LinearLayout, :Button

	$activity.handle_create do |bundle|
	  setTitle 'This is the Title'
      #...

!SLIDE smaller
# assets/scripts/hi_world.rb (cont'd) #
    @@@ruby
	  setup_content do
		linear_layout :orientation => LinearLayout::VERTICAL do
		 @text_view = text_view :text => "What hath Matz wrought?"
		  button :text => "M-x butterfly", :width => :wrap_content
		end
	  end

	  handle_click do |view|
		if view.getText == 'M-x butterfly'
		  @text_view.setText "What hath Matz wrought!"
		  toast 'Flipped a bit via butterfly'
		end
	  end
    end #close handle_create block (prev slide)
