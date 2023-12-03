#### Create your project
```
cd sfdx/projects
sf project generate --name FirstLWC
cd FirstLWC
npm install
npm run lint 
```

#### Enable Dev Hub in Your Org
from vS Code: Command}Shift P, enter sfdx: Authorize a Dev Hub    

from command line run:    
```
sf org login web -d -a LWC-Hub
```

#### Create default scratch org
```
sf org create scratch -s -f config/project-scratch-def.json -a "LWC"
```

#### Create Component    
```
sf lightning generate component --type lwc -n myComponent -d force-app/main/default/lwc
```

#### Push Source to the Scratch Org
```
sf project deploy start
```

#### Pull Source from the Scratch Org
```
sf project retreive start
```

#### Open the scratch Org
```
sf org open
```

[Components Reference](https://developer.salesforce.com/docs/component-library/overview/components)


