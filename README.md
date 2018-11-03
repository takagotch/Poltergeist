### Poltergeist
---
https://github.com/teampoltergeist/poltergeist

```
gem 'poltergist'

require 'capybara/poltergeist'
Capybara.javascript_driver = :poltergeist

Capybara.register_driver :poltergist_debug do |app|
  Capybara::Poltergeist::Driver.new(app, :inspector => true)
end
Capybara.javascript_driver = :poltergeist_debug

page.driver.headers
page.driver.headers = { "User-Agent" => "Poltergeist" }
page.driver.add_headers("Referer" => "https://example.com")
page.driver.headers

page.driver.headers = { "User-Agent" => "Poltergeist" }
page.driver.add_header{"Referer", "http://example.com", permanent: false}
page.driver.headers
visit(login_path)
page.driver.headers

element = find('input#id')
element.send_keys('String')

element.send_keys('H', 'elo', :left, '1')
element.send_keys(:enter)

Capybara.register_driver :poltergeist do |app|
  Capybara::Poltergeist::Driver.new(app, options)
end

page.driver.browser.url_blackist = ['http://www.example.com']
page.driver.brower.url_whitelist = ['http://www.example.com']

click_button "Save"
find_button("Save").trigger('click')

```

```
```

```
```
