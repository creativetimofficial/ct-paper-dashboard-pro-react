# Change Log

## [1.3.2] 2023-05-23

- Update dependencies
- Fix issues

## [1.3.1] 2021-07-08

- Update the dependencies
- Migration to React 18
- Migration to sass from node-sass

## [1.3.0] 2021-05-19

### Bug fixing

- We've change all class components to function ones, so now, Paper Dashboard React accepts hooks
- https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/13
- https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/12

### Major style changes

- Some changes for the `nouislider` styles, since it had a major version change

### Deleted components

### Added components

### Deleted dependencies

- `history` (no longer needed due to the `BrowserRouter`)
- `react-google-maps` (replaced by simple Google Maps API)
- `@types/googlemaps`
- `@types/markerclustererplus`
- `@types/react`
- `ajv` (no longer needed - this was installed so react-scripts install would not show errors)

### Added dependencies

### Updated dependencies

```
bootstrap                      4.5.0   →    4.6.0
chart.js                       2.9.3   →    3.2.1
classnames                     2.2.6   →    2.3.1
match-sorter                   4.1.0   →    6.3.0
moment                        2.26.0   →   2.29.1
node-sass                     4.14.1   →    6.0.0
nouislider                    14.5.0   →   15.1.0
perfect-scrollbar              1.5.0   →    1.5.1
react                        16.13.1   →   17.0.2
react-big-calendar            0.25.0   →   0.33.2
react-bootstrap-sweetalert    5.1.11   →    5.2.0
react-bootstrap-wizard         0.0.7   →    0.0.9
react-chartjs-2                2.9.0   →    3.0.3
react-datetime                2.16.3   →    3.0.4
react-dom                    16.13.1   →   17.0.2
react-notification-alert      0.0.12   →   0.0.13
react-scripts                  3.4.1   →    4.0.3
react-select                   3.1.0   →    4.3.1
react-table                    7.1.0   →    7.7.0
reactstrap                     8.4.1   →    8.9.0
gulp-append-prepend            1.0.8   →    1.0.9
jquery                         3.5.1   →    3.6.0
typescript                     3.9.5   →    4.2.4
```

### Warning

_We will update Bootstrap to v5 when we'll release a new design for the Paper products._
_You will also have the following message: found 80 vulnerabilities (1 low, 79 moderate). This comes from react-scripts, and will be fixed in the next version. NOTE: the product works as expected with these vulnerabilities._
_The following warnings will be thrown on a clean install of the project - NOTE: the product works as expected with these vulnerabilities. - NOTE: we will drop their usage and replace them with other plugins._

```
npm WARN react-datetime@3.0.4 requires a peer of react@^16.5.0 but none is installed. You must install peer dependencies yourself.
npm WARN react-tagsinput@3.19.0 requires a peer of react@^16.0.0 || ^15.0.0 || ^0.14.0 but none is installed. You must install peer dependencies yourself.
```

## [1.2.0] 2020-06-12

### Bug fixing

- Move the `barPercentage` from the `xAxes` to the `datasets` from inside `src/variables/charts.js` to stop warnings from the new Chart.js API
- Add `btnSize=""` to all Sweet Alerts to make the buttons look better
- https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/9 (could not reproduce the issue, so we've left the perfect-scrollbar initialization as is, if there are layout problems, please delete the bits of code specified here: https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/9#issuecomment-590724592)
- https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/8 (solved by the updated dependencies)
- https://github.com/creativetimofficial/ct-paper-dashboard-pro-react/issues/6 - solution to this is to change the usage of the ModalHeader from Reactstrap to simple Bootstrap ones:
  So, instead of:

```
<ModalHeader className="justify-content-center" toggle={this.toggleModalDemo}>
    Modal Title
</ModalHeader>
```

You should use

```
<div className="modal-header justify-content-center">
  <button type="button" className="close" data-dismiss="modal" aria-label="Close" onClick={this.toggleModalDemo}>
    <span aria-hidden="true">×</span>
  </button>
  <h5 className="modal-title">Modal Title</h5>
</div>
```

- Other Paper React products issues solved here as well
  - https://github.com/creativetimofficial/paper-dashboard-react/issues/13
  - https://github.com/creativetimofficial/paper-dashboard-react/issues/12
  - https://github.com/creativetimofficial/paper-dashboard-react/issues/8 (check the jsconfig.json file)
  - https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/2 (check the jsconfig.json file)
  - https://github.com/creativetimofficial/paper-kit-react/issues/2 (check the jsconfig.json file)

### Major style changes

- There will be additional changes in each `.js` and `.html` files since we've used `prettier` to prettify them
- `src/assets/scss/paper-dashboard/_nucleo-outline.scss` (solves https://github.com/creativetimofficial/paper-dashboard-react/issues/8 and https://github.com/creativetimofficial/ct-paper-kit-pro-react/issues/2 and )
- `src/assets/scss/paper-dashboard/react/custom/_nucleo-outline.scss`
- `src/assets/scss/paper-dashboard/react/plugins/_plugin-react-table.scss` (because of the new React-Table API)
- `src/assets/scss/paper-dashboard/react/custom/_modals.scss` (added new styles for modal gooter buttons)
- `src/assets/scss/paper-dashboard/react/plugins/_plugin-react-bootstrap-sweetalert.scss` (due to new Sweet Alert API)
- `src/assets/scss/paper-dashboard/react/custom/_tabs.scss` (vertical tabs had the caret floating from the right border)
- `src/assets/scss/paper-dashboard/react/custom/_responsive.scss` (solves - https://github.com/creativetimofficial/paper-dashboard-react/issues/13)
- `src/assets/scss/paper-dashboard/react/custom/_inputs.scss` (solves - https://github.com/creativetimofficial/paper-dashboard-react/issues/12)

### Deleted components

### Added components

- `src/components/ReactTable/ReactTable.js` (because of the new React-Table API - NOTE: this is just a demo component to showcase the usage of the API, if you wish to add more functionality from the API, you should either duplicate the component, or work over it.)

### Deleted dependencies

### Added dependencies

- match-sorter@4.1.0 (because of the new React-Table API)
- gulp@4.0.2 (for Creative Tim copyrights)
- gulp-append-prepend@1.0.8 (for Creative Tim copyrights)

### Updated dependencies

```
bootstrap                      4.3.1   →     4.5.0
chart.js                       2.8.0   →     2.9.3
history                        4.9.0   →    4.10.1
moment                        2.24.0   →    2.26.0
node-sass                     4.12.0   →    4.14.1
nouislider                    13.1.5   →    14.5.0
perfect-scrollbar              1.4.0   →     1.5.0
react                         16.8.6   →   16.13.1
react-big-calendar            0.21.0   →    0.25.0
react-bootstrap-sweetalert     4.4.1   →    5.1.11
react-chartjs-2                2.7.6   →     2.9.0
react-dom                     16.8.6   →   16.13.1
react-jvectormap              0.0.12   →    0.0.16
react-router-dom               5.0.0   →     5.2.0
react-scripts                  3.0.1   →     3.4.1
react-select                   3.0.3   →     3.1.0
react-table                   6.10.0   →     7.1.0
reactstrap                     8.0.0   →     8.4.1
@types/googlemaps             3.36.2   →    3.39.6
@types/react                 16.8.19   →   16.9.35
ajv                           6.10.0   →    6.12.2
jquery                         3.4.1   →     3.5.1
typescript                     3.5.1   →     3.9.5
```

### Warning

_All the following products: Paper Kit React, Paper Dashboard React, Paper Kit PRO React and Paper Dashboard PRO React have been updated together, and thus, we've added to all of them the same version of 1.2.0 - we may have skipped some versions for some of the above products, we've done so, since we want all Paper & React products to share the same versions._
_While in development some of the plugins that were used for this product will throw some warnings - note, this only happens in development, the UI or the functionality of the product is not affected, also, if the issues will persist in React 17, we'll drop usage of those plugins, and replace them with other ones._
_Warnings might appear while doing an npm install - they do not affect the UI or the functionality of the product, and they appear because of NodeJS and not from the product itself._

## [1.1.0] 2019-05-31

### Major changes

- Changed the styles found inside `src/assets/scss/*`
- Renamed `src/layouts/Admin/Admin.jsx` to `src/layouts/Admin.jsx`
- Renamed `src/layouts/Auth/Auth.jsx` to `src/layouts/Auth.jsx`

### Dropped components

### Added components

### Deleted dependencies

### Added dependencies

### Updated dependencies

- @types/googlemaps 3.30.16 → 3.36.2
- @types/react 16.7.1 → 16.8.19
- ajv 6.5.5 → 6.10.0
- bootstrap 4.1.3 → 4.3.1
- chart.js 2.7.3 → 2.8.0
- history 4.7.2 → 4.9.0
- jquery 3.3.1 → 3.4.1
- moment 2.22.2 → 2.24.0
- node-sass 4.9.4 → 4.12.0
- nouislider 12.1.0 → 13.1.5
- prop-types 15.6.2 → 15.7.2
- react 16.6.0 → 16.8.6
- react-big-calendar 0.20.2 → 0.21.0
- react-bootstrap-wizard 0.0.5 → 0.0.7
- react-chartjs-2 2.7.4 → 2.7.6
- react-datetime 2.16.2 → 2.16.3
- react-dom 16.6.0 → 16.8.6
- react-jvectormap 0.0.4 → 0.0.12
- react-notification-alert 0.0.8 → 0.0.12
- react-router-dom 4.3.1 → 5.0.0
- react-scripts 2.0.5 → 3.0.1
- react-select 2.1.1 → 3.0.3
- react-table 6.8.6 → 6.10.0
- reactstrap 6.5.0 → 8.0.0

## [1.0.0] 2018-11-14

### Original Release

- Added Reactstrap as base framework
- Added design from Paper Dashboard 2 PRO by Creative Tim
