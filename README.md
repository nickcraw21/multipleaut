# multipleaut

          <!-- laat addres zien die bij user hoort -->
                            @foreach($user as $row)
                                @if($row->name == $invoicetId->name)

                                    {{ $row->street }}
                                    {{ $row->number }}
                                @endif
                            @endforeach

                            <!-- laat prijs zien die bij doctor hoort -->
                            @foreach($doctor_request as $row)
                                @if($row->name == $appointmentId->doctor)
                                    {{ $row->price }}
                                    {{ $row ->name }}
                                @endif
                            @endforeach

                            @foreach($doctor_request as $row)
                                @if($row->name == $appointmentId->lunch)
                                    {{ $row->price }}
                                    {{ $row ->name }}
                                @endif
                            @endforeach
