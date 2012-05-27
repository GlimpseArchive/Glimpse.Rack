Glimpse.Rack
=======================================

Glimpse for Rack - A client side Glimpse into whats going on in your server


Rack Server Module
=======================================

The Glimpse "theory of operation" is such that server modules (`plugins`) expose
application, configuration, diagnostic, or environment information. The
Glimpse Ruby offering is provided as Rack middleware.


Installation
=======================================

    % gem install glimpse


Configuration
=======================================


    # add a use line to your builder
    require 'rack/glimpse'
    Rack::Builder.new do
      use Rack::Glimpse, {
        :glimpse          => { :enabled => false, :request_limit => '15', :logging_enabled => false, :cache_enabled => true, :ip_forwarding_enabled => false },
        :ip_addresses     => {},
        :plugin_blacklist => {},
        :url_blacklist    => {},
        :content_types    => {},
        :environments     => {}
      }

      run Hello.new
    end


Creating Plugins
=======================================

Read the [documentation][3] for more information.


Contributing
=======================================

# Obtain the project (assumes you've forked it)

    % cd ~/projects
    % git clone git@github.com:user/Glimpse.Rack.git && cd Glimpse.Rack
    % bundle install

# Run Tests

    % bundle exec rake test


License
=======================================

Glimpse is licensed under the ??? license.










[1]: http://getglimpse.com
[2]: http://getglimpse.com/Protocol
[3]: http://getglimpse.com/Help/CreatingPlugins
