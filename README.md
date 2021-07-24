# EmojiScript Cloud Hub AI

Example showcase:
```typescript
import * as React from "react";
import { useState } from "react";
import { Button } from "@blueprintjs/core";
import { getNewModalInstance } from "src/components/modals/genericModal/GenericModalView";
import { ModifyUnitTypeView } from "src/components/domains/unitConversion/modals/unitType/modifyUnitTypeModal/ModifyUnitTypeView";
import { localeUtils } from "src/testUtils/locale";
import { unitConversionApi } from "src/generated-code/api/unitConversionApi";
import UnitType = unitConversionApi.models.UnitType;

/**
 * Displays unit type. Mock to be deleted after merge of Christian's changes.
 * @param unitType is unit type to display.
 * @param updateOnChange is callback to refresh when unit type is changed.
 * @constructor
 */
export const UnitTypeMock = ({
    unitType,
    updateOnChange
}: {
    /**
     * Unit type to display.
     */
    unitType: UnitType;
    /**
     * Callback to refresh when unit type is changed.
     * @param unitType is unit type to update.
     */
    updateOnChange: (unitType: UnitType) => void;
}) => {
    const [generatedUUID, setGeneratedUUID] = useState("");

    return (
        <div>
            {JSON.stringify(unitType)}

            <div>
                <Button
                    text={"Change"}
                    onClick={() => {
                        setGeneratedUUID(getNewModalInstance());
                    }}
                />
                <ModifyUnitTypeView
                    onSave={(name: string) => {
                        updateOnChange({ ...unitType, name: name });
                    }}
                    localeUtils={localeUtils}
                    isUnitTest={false}
                    currentModalInstanceId={generatedUUID}
                    unitType={unitType}
                />
            </div>
        </div>
    );
};
```

becomes

```typescript
import * as React from "react";
import { useState } from "react";
import { Button } from "@blueprintjs/core";
import { getNewModalInstance } from "src/components/modals/genericModal/GenericModalView";
import { ModifyUnitTypeView } from "src/components/domains/unitConversion/modals/unitType/modifyUnitTypeModal/ModifyUnitTypeView";
import { localeUtils } from "src/testUtils/locale";
import { unitConversionApi } from "src/generated-code/api/unitConversionApi";
import UnitType = unitConversionApi.models.UnitType;

/**
 * Displays unit type. Mock to be deleted after merge of Christian's changes.
 * @param unitType is unit type to display.
 * @param updateOnChange is callback to refresh when unit type is changed.
 * @constructor
 */
export const UnitTypeMock = ({
    unitType,
    updateOnChange
}: {
    /**
     * Unit type to display.
     */
    unitType: UnitType;
    /**
     * Callback to refresh when unit type is changed.
     * @param unitType is unit type to update.
     */
    updateOnChange: (unitType: UnitType) => void;
}) => {
    const [generatedUUID, setGeneratedUUID] = useState("");

    return (
        <div>
            {JSON.stringify(unitType)}

            <div>
                <Button
                    text={"Change"}
                    onClick={() => {
                        setGeneratedUUID(getNewModalInstance());
                    }}
                />
                <ModifyUnitTypeView
                    onSave={(name: string) => {
                        updateOnChange({ ...unitType, name: name });
                    }}
                    localeUtils={localeUtils}
                    isUnitTest={false}
                    currentModalInstanceId={generatedUUID}
                    unitType={unitType}
                />
            </div>
        </div>
    );
};
```



## Repo Structure


## How to Set Up


## How to Run in Development


## How to Test


## How to Build


## How to Run in Production


## Miscellaneous


## Additional Resources

