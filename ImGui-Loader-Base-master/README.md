# ImGui Loader Base
 A Base For a Loader or literally anything.


# IF YOU  HAVE ANY QUESTIONS DM ME ON DISCORD! Herb.#0001


In the folder ui, there will be ui.cc, look for "// Your code here" thats where you will put the code
to create stuff like a checkbox or a button.





#VARIABLES!!!

Globals.hh is where you will put all your vairbales *in the class

For *var* is where you will put the variable name

if my variable was: 

bool ex = false;

I would replace *var* with:

globals.ex


#EXAMPLES!!!

some basic examples to put in "// Your code here":

if (ImGui::BeginTabBar("MAIN")) // basic tab bar for a cheat taken from my source
                {
                    if (ImGui::BeginTabItem("  MAIN  "))
                    {



                        ImGui::EndTabItem();
                    }

                    if (ImGui::BeginTabItem("  MISC  "))
                    {
                        ImGui::Checkbox("Bhop", &*var*);

                        ImGui::EndTabItem();
                    }

                    if (ImGui::BeginTabItem("  VISUALS  "))
                    {
                        ImGui::Checkbox("Glow", &g*var*); // checkboxes take bools
                        if (glow == true)
                        {
                            ImGui::ColorEdit4("Team color", *var*);
                            ImGui::SliderFloat("Team brightness", &*var*, 0.f, 5.f);
                            ImGui::Text("");
                            ImGui::ColorEdit4("Opp color", *var*);
                            ImGui::SliderFloat("Opp brightness", &*var*, 0.f, 5.f); // sliders need a min value, and max.
                            ImGui::Text("");
                        }
                        ImGui::SliderInt("FOV", &*var*, 30.f, 170.f);


                        ImGui::EndTabItem();
                    }
                    ImGui::EndTabBar();
                }