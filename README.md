# SampleTestProj

SELECT  C.CategoryName,A.AdminEmail,A.AdminFirstName,C.MODIFIEDDATE FROM  [dbo].[Category](NOLOCK) C 
JOIN [dbo].[Admin](NOLOCK) A ON A.AdminID=C.AdminID
WHERE C.CategoryTypeID=1 AND C.AdminID IS NOT NULL AND C.AdminID <> 0 AND C.ModifiedDate < GETUTCDATE()-4
