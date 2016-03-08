# Factory Girl Sequence Reset

Seringkali kita melihat `sequence` dalam file factory dari FactoryGirl. Syntax ini digunakan untuk membuat urutan dalam attribute suatu object.

```ruby
FactoryGirl.define do
  factory :user do
    sequence(:email) { |n| "person#{n}@example.com" }
  end
end

create(:user).email # => "person1@example.com"
create(:user).email # => "person2@example.com"
```

Namun hal ini akan menjadi suatu masalah jika dalam satu test kita menge-set value email menjadi `"person1@example.com"` padahal kita pernah melakukan `create` di test case lainnya. Sequence dalam Factory Girl tidak otomatis ter-reset dalam setiap test case. Jika kita memang membutuhkan hal tersebut, kita dapat membuat callback `after` untuk setiap kali menjalankan test case.

```ruby
# Rspec - spec_helper.rb
RSpec.configure do |config|
  config.after(:each) do |example|
    FactoryGirl.reload
  end
end

# TestUnit - test_helper.rb
class ActiveSupport::TestCase
  def teardown
    FactoryGirl.reload
  end
end
```

`FactoryGirl.reload` akan me-reset sequence dari 0 (nol) kembali setiap selesai menjalankan test.
