
@php
+                                                        $expirationDate = new \DateTime();
+                                                        $expirationDate->sub(new \DateInterval("P7Y"));
+                                                        $invoiceDate = \DateTime::createFromFormat("Y-m-d", $row->date);
+
+                                                        if ($expirationDate < $invoiceDate) {
+                                                            echo "disabled";
+                                                        }
+ @endphp
+                                                       
