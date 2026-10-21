cmake_minimum_required(VERSION 3.22)
project(JuceAudioApp VERSION 1.0.0)

add_subdirectory(JUCE)

juce_add_console_app(JuceAudioApp
    PRODUCT_NAME "JUCE Audio App"
)

target_sources(JuceAudioApp PRIVATE main.cpp)

target_link_libraries(JuceAudioApp
    PRIVATE
        juce::juce_core
        juce::juce_events
        juce::juce_audio_basics
        juce::juce_audio_devices
)
