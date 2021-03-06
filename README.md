**gosh**\
gosh is a simple yet fast API to shorten URLs made using go-lang.

**packages used** --\
[gorm.io/gorm](https://gorm.io/) & [gorilla/mux](https://github.com/gorilla/mux/)

**get started** --\
send a POST request to https://u.gosh.ga/api/create with a JSON body like this:

```json
{
    "slug": "my_unique_slug",
    "target_url": "https://foo-bar.com/"
}
```

**api methods** --\
`GET` - `https://u.gosh.ga/api/[slug]` - return the data for given slug.\
`POST` - `https://u.gosh.ga/api/create` - create a new slug data.\
`GET` - `https://u.gosh.ga/[slug]` - redirects to target_url for given slug.

**example** --\
https://u.gosh.ga/ashish redirects to https://github.com/asheeeshh i.e. my github profile!

If you send a GET request to https://u.gosh.ga/api/get/ashish. it will return this --\

```json
{
    "slug": "ashish",
    "target_url": "https://github.com/asheeeshh"
}
```

**note** --\
the project is still a WIP, bugs and issues are expected, please please please let me know if you come across one! i'll also be making a frontend for this project which would soon be live at https://gosh.ga/ allowing everyone to shorten URLs without making api requests :)
